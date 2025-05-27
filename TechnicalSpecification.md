# Technical Specification

## Introduction

This project was commissioned by the Intermarché of Saint-Rémy-de-Provence. The goal is to help the customers to choose which wine and cheese would be the best fit for the dish they plan to cook. This application will be made using Bubble and will focus on delivering an intuitive user experience, highlighting local products, and showcasing well-matched options at different price points.

---

## Technical Overview


### Requirements




## Bubble Implementation

### Pages 
The application will be structured across several pages to improve performance and simplify team collaboration. Each of them will focus on a different task or user goal, which will help for clarity. 

The planned pages include:

- `index`: Homepage where users are welcomed and guided to begin the process. It contains the primary entry point for selecting a dish and starting the recommendation flow.
- `dish_lists`: Displays wine and cheese suggestions, grouped by category.
- `recommendation`: Shows detailed product matches for the selected dish.
- `favorite`: Lets users view and manage the products they labelled as favorite.
- `profile`: Allows users to update preferences such as dietary restrictions, allergies, and language.
- `onboarding`: Guides new users through initial preference setup.
- `reset_pw`: For password recovery and reset.

---

### Reusable Elements

To keep the project modular and easy to maintain, several repeating parts of the UI will be built as reusable elements. These components will be used across multiple pages to ensure consistency and avoid duplicating logic or design. They’ll handle features such as navigations bars, cheese and wine cards and product details. 

---

### Workflows (?)

---

### Custom States (?)

---

### Data Types (?)

---

### Styles

To ensure consistency and maintanability in the design, all UI components will be styled using Bubble's built-in Styles page.  
No inline styles will be used unless required for dynamic conditional logic.

---


technical requirements -> how will it be done: 

system architecture (? bubble check bubble team account)

performance goal?

harwdware used (irelevant)

details on how will the database work (tbd) <br>




On bubble:

how was figma was/willbe used + implemented? (tbd with func/pierre)
bubble screenshots/diagrams (flow charts, will be done when available)

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





data type example:

**Name:** Product  
**Fields:**  
- name (text): The product name  
- category (option set): 'Wine' or 'Cheese'  
- image (image): Product image  
- origin (text): Region or country  
- pairing_tags (list of texts): Tags for dish pairing logic  
- price (number): In euros  
- isLocal (yes/no): Highlights local products  
- TBD (TBD): Link to a similar product
- 





technical architecture
    - software choices? (figma)
    - ? 


<br>
more details -> manech intermarché



maybe exterior document for the conventions https://github.com/algosup/2023-2024-project-4-sportshield-team-8/blob/main/documents/technicalSpecifications/technicalSpecifications.md#conventions
take exaple from this 
 the part about coding would be potential conventions on bubbbble. 

> [!NOTE]
> test <br>




