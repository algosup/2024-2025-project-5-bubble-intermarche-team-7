# Technical Specification

## Introduction

This project was commissioned by the Intermarché of Saint-Rémy-de-Provence. The goal is to help the customers to choose which wine and cheese would be the best fit for the dish they plan to cook. This application is being made on Bubble and will focus on delivering an intuitive user experience, highlighting local products, and showing well-matched options at different price points.

---

## Technical Overview

Search, filters, and dynamic recommendations will be handled through a combination of search boxes, dropdowns, and custom states. Repeating groups will be used to display filtered lists of products based on user input and preferences. Option sets will be used for tags like allergies, dietary restrictions, or taste profiles, which makes filtering both more reliable and easier to update. Reusable elements will be used for anything that appears across several pages, like navigation bars or product cards, to keep things clean and consistent.

---

## Bubble Implementation

### Pages 
The application will be structured across several pages to improve performance and simplify team collaboration. Each of them will focus on a different task or user goal, which will help for clarity. 

The planned pages include:

- `index`: Homepage where users are welcomed and guided to begin the process. It contains the primary entry point for selecting a dish and starting the recommendation flow.
- `dish_lists`: Displays wine and cheese suggestions, grouped by category.
- `favorite`: Lets users view and manage the products they labelled as favorite.
- `profile`: Allows users to update preferences such as dietary restrictions, allergies, and language.
- `onboarding`: Guides new users through initial preferences setup.
- `404`: This page will appear if the user tries to go to an unexisting page or destination.

---

### Reusable Elements

To keep the project modular and easy to maintain, several repeating parts of the UI will be built as reusable elements. These components will be used across multiple pages to ensure consistency and avoid duplicating logic or design. They’ll handle features such as navigations bars, cheese and wine cards and product details. 

---

### Workflows

Workflows will handle all user interactions and app logic such as navigation, filtering, or showing/hiding elements. Each workflow must follow the naming convention. Complex logic must be broken down into multiple workflows when necessary, to keep everything clear and easy to debug.

---
 
### Styles

To ensure consistency and maintanability in the design, all UI components will be styled using Bubble's built-in Styles page. No inline styles will be used unless required for dynamic conditional logic. This will allow us to (if needed) update the entire app theme from one place.

---

### Custom States

Custom states will be used to store temporary values that do not need to be saved to the database, which will be ideal for controlling UI behavior such as toggling elements or, tracking selected filters.  They also should be added directly to the element they control, rather than to the page or unrelated containers. This keeps the logic easy to understand, limits unwanted side effects, and makes future changes easier.

---

### Product Display (Cards)

Wine, cheese, and dish products are displayed using three dedicated Reusable Elements: `wineCards`, `cheeseCards`, and `dishRowCards`. Each of them contains a repeating group sorted by product type, with a consistent card layout showing relevant product details.

---

#### Wine Card

| **Property**               | Dynamic Source                                                                 | Style / Settings                                                     |
|------------------------|--------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| **Card dimensions**    | 145 × 330 px                                                                    | Min-width 145px / Max-width 185px<br>Min-height 0 / Max-height 330 px  |
| **Responsive widths**  | `<768px` → 140px  | `≤992px` → 215px  | `>992px` → 210px                                   |
| **Product image**      | `Parent group's Product's image`                                               | 65 × 205 px, Zoom rendering                                          |
| **Year**               | `Parent group's Product's year`                                                | Arial 12px, weight 400                                                |
| **Name**               | `Parent group's Product's name`                                                | Montserrat 16px, weight 800, color `#231918`                          |
| **Technical details**  | `origin`, `wine_type`, `volume_or_weight`, `price_per_liter_or_kg` (rich text) | Arial 12px, weight 400, color `#231918`, line-spacing 1.4             |
| **Price**              | `Parent group's Product's price`                                               | Montserrat 26px, weight 800                                           |
| **Favorite icon**      | Two overlapping MaterialIcons (35 × 35 px)                                     | Bottom-right (absolute position)                                     |
| • `favorite_outline`   | Visible when Current User’s `favorites` **does not** contain the product       | on-click → “Add to favorites”                                        |
| • `favorite`           | Visible when Current User’s `favorites` **does** contain the product           | on-click → “Remove from favorites”                                   |

---

#### Cheese Card

| **Property**                | Dynamic Source                                             | Style / Settings                     |
|-------------------------|-------------------------------------------------------------|---------------------------------------|
| **Card dimensions**     | 230 × 305 px                                                | Fixed width & height                  |
| **Product image**       | `Parent group's Product's image`                           | Aspect-fit                            |
| **Label badges**        | RepeatingGroup on `List of Tags` (e.g. Local, blue cheese) | Inline-flex badges, margin-right 4px  |
| **Name**                | `Parent group's Product's name`                            | Montserrat 16px, weight 800           |
| **Description**         | `Parent group's Product's description`                     | Arial 12px, weight 400, color #231918 |
| **Weight & unit price** | `volume_or_weight` + `" | "` + `price_per_liter_or_kg`      | Arial 12px, weight 400                |
| **Price**               | `Parent group's Product's price`                           | Montserrat 26px, weight 800           |
| **Favorite icon**       | Same logic as Wine                                          | 35 × 35 px, bottom-right              |

---

#### Dish Card

| Property               | Dynamic Source                          | Style / Settings               |
|------------------------|------------------------------------------|--------------------------------|
| **Card dimensions**    | 135 × 290 px                             | Fixed width & height           |
| **Product image**      | `Parent group's Product's image`        | Cover, full-width              |
| **Dish name**          | `Parent group's Product's name`         | Montserrat 16px, weight 800    |
| **Favorite icon**      | Same logic as Wine & Cheese             | 35 × 35 px, bottom-right       |

---

#### Favorites Logic

This will be shared across all the cards

- **Add to favorites**:  
  Trigger → icon `favorite_outline`  
  Action → “Make changes to Current User” → `favorites add Current cell's Product`

- **Remove from favorites**:  
  Trigger → icon `favorite`  
  Action → “Make changes to Current User” → `favorites remove Current cell's Product`

---

## Data Base Structure

The app will use a structured data model to store and manage the different types of products (dishes, wines, cheeses), as well as user preferences. The database will be designed to allow fast filtering, personalized suggestions, and compatibility with features such as favorites, allergy filters, or local product highlighting.

---

### Products 

This type will be used for every physical product — dish, wine, or cheese — displayed in the app. Each entry will include product metadata, pricing, origin, tags for filtering, and store-related info.

**Name:** Product  
**Fields:**
- `name` (text): The product name  
- `description` (text): Short or detailed product description  
- `image` (image): Visual used in product cards and detail views  
- `origin` (text): Region or country of origin (used to highlight local items)  
- `price` (number): Price in euros  
- `volume_or_weight` (text): Format such as 75cl or 200g  
- `price_per_liter_or_kg` (text): Calculated price per standard unit  
- `type` (ProductType - Option Set): Used to distinguish between dishes, wines, and cheeses  
- `is_alcohol` (yes / no): Whether the product is alcoholic or not  
- `is_expert_pick` (yes / no): Used to highlight selected recommendations  
- `store_location` (text): Indicates where the product can be found in the store  
- `taste_notes` (List of TasteNote): Fruity, Spicy, Earthy...  
- `allergy_tags` (List of Allergy): Useful for hiding incompatible products  
- `diet_tags` (List of DietaryRestriction): Vegan, Vegetarian, etc. 
- `wine_year` Year of wine production (empty for cheeses). 
---

### User

Stores user preferences for language, budget, dietary restrictions, and favorites.

| Field               | Type                          | Multiple Entries | Description                                   |
|--------------------|-------------------------------|------------------|-----------------------------------------------|
| `first_name`       | text                          | No               | Optional user name for personalization        |
| `email`            | text                          | No               | Optional email (used only for future exports) |
| `language`         | Languages (Option Set)        | No               | Preferred language for UI                     |
| `budget_per_bottle`| number                        | No               | Max budget preference for wine                |
| `allergies`        | List of Allergy               | Yes              | Active allergy preferences                    |
| `diet_preferences` | List of DietaryRestriction    | Yes              | Vegan, Vegetarian, etc.                       |
| `favorites`        | List of Products              | Yes              | User-saved products                           |
| `search_history`   | List of text or Dishes        | Yes              | Last searched dishes (max 6)                  |

--- 

## Conventions

### On GitHub
 
- All files and folders should be named in PascalCase.
- Technical, Functional and Management documentation should be in their own dedicated folder in a ./documents folder.
- Images should be in an ./image subfolder from where they are called.
- GitHub branches should be named in kebab-case.

### On Bubble

To maintain consistency and reliability during development, the following naming and structuring conventions must be followed across all pages, elements, workflows, custom states, and styles in the Bubble application.

####  Page Naming

Each page must be named using **snake_case**, describing the content or structure it displays.

**Examples:**
- `home_page`
- `dish_lists`
- `search_results`
- `profile_settings`

---

#### Repeating Group Naming

Repeating groups must follow the format: rg_function

Where:
- `rg` stands for repeating group
- `function` describes the content or role

**Examples:**
- `rg_productList`
- `rg_filteredResults`
- `rg_userFavorites`

---

#### Element Naming

All the elements must follow the following convention: type_function_index

Where:
- `type` = element type (e.g., `button`, `group`, `input`, `icon`)
- `function` = what it does or represents
- `index` = optional number for disambiguation

**Examples:**
- `button_popup_2`
- `group_mailInput`
- `input_dishSearch`

The point is to avoid names such as `Text A` or `Group B`.

---
#### Workflow Naming

Workflows must be written using *camelCase.* They must be short, action-oriented and clearly describe what the workflow does. 

Here is the needed format: `eventActionResult`

Where:
- `event` = the trigger (button click, page load)
- `action` = the main behavior
- `result` = what the outcome is, if needed for clarity


The goal is to avoid vague names such as `workflow1` or `popupLogic`. 




---

