# Technical Specification

## Introduction

This project was commissioned by the Intermarché of Saint-Rémy-de-Provence. The goal is to help the customers to choose which wine and cheese would be the best fit for the dish they plan to cook. This application will be made using Bubble and will focus on delivering an intuitive user experience, highlighting local products, and showcasing well-matched options at different price points.

---

### Technical Overview









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

work is done on several pages to simplify workload
define styles.. 
worfklow names, state names,

search feature, onboarding feature, profil page missing

name of the element_function (+ number if necessary) ex: button_popup_2 or groupe_mailinput (to develop)


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




