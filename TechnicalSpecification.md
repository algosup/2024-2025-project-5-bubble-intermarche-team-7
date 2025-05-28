# Technical Specification

## Introduction

This project was commissioned by the Intermarché of Saint-Rémy-de-Provence. The goal is to help the customers to choose which wine and cheese would be the best fit for the dish they plan to cook. This application will be made using Bubble and will focus on delivering an intuitive user experience, highlighting local products, and showcasing well-matched options at different price points.

---

## Technical Overview


### Requirements

<!-- The app will be built entirely using Bubble and will rely on its no-code visual tools to deliver all the expected features.  -->

Search, filters, and dynamic recommendations will be handled through a combination of search boxes, dropdowns, and custom states. Repeating groups will be used to display filtered lists of products based on user input and preferences. Option sets will be used for tags like allergies, dietary restrictions, or taste profiles, which makes filtering both more reliable and easier to update. Reusable elements will be used for anything that appears across several pages, like navigation bars or product cards, to keep things clean and consistent.




## Bubble Implementation

### Pages 
The application will be structured across several pages to improve performance and simplify team collaboration. Each of them will focus on a different task or user goal, which will help for clarity. 

The planned pages include:

- `index`: Homepage where users are welcomed and guided to begin the process. It contains the primary entry point for selecting a dish and starting the recommendation flow.
- `dish_lists`: Displays wine and cheese suggestions, grouped by category.
- `favorite`: Lets users view and manage the products they labelled as favorite.
- `profile`: Allows users to update preferences such as dietary restrictions, allergies, and language.
- `onboarding`: Guides new users through initial preference setup.
- `404`: This page will appear if the user tries to go to an unexisting page or destination. (cleaner version needed)

---

### Reusable Elements

To keep the project modular and easy to maintain, several repeating parts of the UI will be built as reusable elements. These components will be used across multiple pages to ensure consistency and avoid duplicating logic or design. They’ll handle features such as navigations bars, cheese and wine cards and product details. 

---

### Workflows

Workflows will handle all user interactions and app logic such as navigation, filtering, or showing/hiding elements. Each workflow must follow the naming convention. Complex logic must be broken down into multiple workflows when necessary, to keep everything clear and easy to debug.

---

### Custom States

Custom states will be used to store temporary values that do not need to be saved to the database, which will be ideal for controlling UI behavior such as toggling elements or, tracking selected filters.  They also should be added directly to the element they control, rather than to the page or unrelated containers. This keeps the logic easy to understand, limits unwanted side effects, and makes future changes easier.
---

### Styles

To ensure consistency and maintanability in the design, all UI components will be styled using Bubble's built-in Styles page. No inline styles will be used unless required for dynamic conditional logic. This will allow us to (if needed) update the entire app theme from one place.

---

### Data Base Structure

The app will use a structured data model to store and manage the different types of products (dishes, wines, cheeses), as well as user preferences. The database will be designed to allow fast filtering, personalized suggestions, and compatibility with features such as favorites, allergy filters, or local product highlighting.

#### Products 

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

#### User

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







diagrams missing (flow charts)

## Conventions

### On GitHub
 
- All files and folders should be named in PascalCase.
- Technical, Functional and Management documentation should be in their own folder in a ./documents folder.
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





<br>
more details -> manech intermarché



maybe exterior document for the conventions https://github.com/algosup/2023-2024-project-4-sportshield-team-8/blob/main/documents/technicalSpecifications/technicalSpecifications.md#conventions
take exaple from this 
 the part about coding would be potential conventions on bubbbble. 

> [!NOTE]
> test <br>




image + description missing for attributes
