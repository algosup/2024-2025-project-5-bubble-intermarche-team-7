<h1 align="center"> Functional Specification Document </h1>

<p align="center">
Created by: Quentin CLÉMENT <br> Creation Date: 30/04/2025 <br> Last Update: 16/05/2025
</p>

<details>
<summary>

## Table of Contents

</summary>

- [Table of Contents](#table-of-contents)
- [1. Introduction](#1-introduction)
  - [1.1 Purpose of the Document](#11-purpose-of-the-document)
  - [1.2 Intended Audience](#12-intended-audience)
  - [1.3 Scope of the Application](#13-scope-of-the-application)
  - [1.4 Definitions and Acronyms](#14-definitions-and-acronyms)
- [2. Overall Description](#2-overall-description)
  - [2.1 Product Perspective](#21-product-perspective)
  - [2.2 Product Functions Summary](#22-product-functions-summary)
  - [2.3 User Characteristics](#23-user-characteristics)
  - [2.4 Assumptions and Dependencies](#24-assumptions-and-dependencies)
  - [2.5 Design and Implementation Constraints](#25-design-and-implementation-constraints)
- [3. Use Case Scenarios](#3-use-case-scenarios)
    - [3.1 Base Use Case: User Has a Meal or Ingredient in Mind](#31-base-use-case-user-has-a-meal-or-ingredient-in-mind)
    - [3.2 Base Use Case: User Doesn’t Have a Meal in Mind](#32-base-use-case-user-doesnt-have-a-meal-in-mind)
    - [3.3 Base Use Case: User Selects from Favorites](#33-base-use-case-user-selects-from-favorites)
    - [3.4 Contextual Differences](#34-contextual-differences)
- [4. Functional Requirements](#4-functional-requirements)
    - [4.1 Offline Functionality](#41-offline-functionality)
    - [4.2 Favorites System](#42-favorites-system)
    - [4.3 Navigation Structure](#43-navigation-structure)
    - [4.4 Search Logic](#44-search-logic)
    - [4.5 Performance Assumptions](#45-performance-assumptions)
    - [4.6 Localization / Multilingual Support](#46-localization--multilingual-support)
    - [4.7 Caching and Data Persistence](#47-caching-and-data-persistence)
    - [4.8 First-Time User Experience](#48-first-time-user-experience)
    - [4.9 Error and Empty State Handling](#49-error-and-empty-state-handling)
    - [4.10 First-Time User Experience](#410-first-time-user-experience)
- [5. Page-by-Page Description](#5-page-by-page-description)
    - [5.1 Navigation Bar](#51-navigation-bar)
    - [5.2 Homepage](#52-homepage)
    - [5.3 Recipe List Screen](#53-recipe-list-screen)
    - [5.4 Meal or Ingredient Screen](#54-meal-or-ingredient-screen)
    - [5.5 Product Detail Page](#55-product-detail-page)
    - [5.6 Favorites Page](#56-favorites-page)
    - [5.7 Profile Page](#57-profile-page)

</details>

## 1. Introduction  

### 1.1 Purpose of the Document  
The aim of this document is to present the functional specifications of the Intermarché wine and cheese recommendation application. These functional specifications were developed in accordance with the client’s requirements and the technical constraints defined by both the client and the target production environment.

### 1.2 Intended Audience  
The target audience for this spec are the developers, testers and documenters of the application. In addition, people charged with the maintenance of the application will also be able to refer to this document.

### 1.3 Scope of the Project  
The scope of the project is to design and develop the front-end of Intermarché’s wine and cheese recommendation application. The objective is to support the supermarket’s business strategy by fostering customer engagement and loyalty, while increasing the average basket size and overall profitability.

### 1.4 Definitions and Acronyms

---

## 2. Overall Description  
### 2.1 Product Perspective  
This application is intended to operate independently from Intermarché’s existing digital ecosystem, such as the national website and mobile app. It is being developed specifically for the Intermarché store located in Saint-Rémy-de-Provence. As such, the product database will be limited to the inventory and product offerings of that specific store, rather than the full Intermarché catalog.

Despite being a standalone product, the application will be designed with future integration in mind. To facilitate potential incorporation into Intermarché’s broader digital platforms, the application will adhere to the brand’s graphic charter and general design guidelines.

### 2.2 Product Functions Summary  
- Wine and cheese pairing suggestions based on the user’s selected meal.
- Budget-based recommendations, offering three different wine and cheese options per meal to suit varying price ranges.
- Dietary adaptation, filtering recommendations according to dietary restrictions such as vegetarian preferences or specific allergies.
- Curated meal suggestions, including seasonal recipes, regional specialties, trending dishes, and low-budget options.
- Product detail pages for each wine and cheese, displaying information such as origin, appellation, tasting notes, and other relevant characteristics.
- Favorites feature, allowing users to save and quickly access preferred products.
- In-store product locator, indicating the aisle or shelf where a selected product can be found.

### 2.3 User Characteristics  
The two main target audiences for the application are:
1. **Everyday Shoppers**: \
These are regular customers who visit the Intermarché store frequently, often for routine grocery shopping. They tend to be budget-conscious and may not initially intend to purchase wine or cheese. The application will focus on encouraging impulse purchases by recommending affordable pairings that complement their existing basket, with the goal of increasing the average spend per visit.
2. **Tourists**: \
Visitors to the region, particularly those unfamiliar with local products, represent a second key audience. Tourists are typically more open to spending on premium items, especially regional specialties that offer a unique or authentic experience. The application will cater to this group by highlighting curated selections of local wines and cheeses, presented as memorable or gift-worthy purchases to enhance their visit.

### 2.4 Assumptions and Dependencies  
The development and successful operation of the application are based on the following assumptions and dependencies:

### Assumptions
- The Saint-Rémy-de-Provence Intermarché store will provide access to a structured, up-to-date product database, including pricing, in-store locations, and product pairings.
- Store staff or IT support will maintain and update the product inventory regularly.
- Users will have internet access while inside the store, either via mobile data or store-provided Wi-Fi. However, the client has expressed the desire for the app to remain partially functional in offline mode.

### Dependencies
- The mobile app will rely on at least one external service or internal logic engine to generate food–wine–cheese pairings.
- Availability of brand assets and design guidelines from Intermarché to ensure compliance with the graphic charter.
- Data privacy and legal compliance (e.g., GDPR) must be ensured through client-provided guidelines or internal policy support.

## 2.5 Design and Implementation Constraints

- **Platform and Technology Stack**: The application must be compatible with both Android and iOS devices. It will be developed using Bubble.io, a no-code platform that supports cross-platform deployment. The app must offer a consistent and responsive user experience across supported devices.
- **Device Compatibility**: The application must perform efficiently on mid-range smartphones commonly used by the target audience. It should support older operating systems, with a minimum requirement of Android 5.0 and iOS 12.0. Responsive design principles must be applied to accommodate varying screen sizes and resolutions.
- **Offline Functionality**: In line with client expectations, the application must include partial offline capabilities (e.g., caching product data). Full offline support is not required.
- **Front-End Scope Only**: This project is limited to front-end development. Server-side components such as the pairing engine and data services are outside the current scope and must be developed separately. However, the front-end must be structured to allow smooth integration with future back-end systems.
- **Data Source and API Readiness**: During the initial phase, the app will use CSV files provided by the client to simulate product and pairing data. The architecture must remain flexible to enable future integration with the Intermarché product database and additional APIs for dynamic pairing suggestions.
- **Design Compliance**: The user interface must strictly adhere to Intermarché’s official graphic charter, including the use of brand colors, typography, and logo placement. Any deviations must be validated by the client.
- **Third-Party Component Approval**: Any third-party libraries, plugins, or services used (e.g., for analytics, media, or localization) must be submitted for client approval to ensure license compliance and long-term maintainability.
- **Regulatory Compliance**: The application must comply with relevant legal and data protection regulations, particularly the General Data Protection Regulation (GDPR), even if no persistent user data is collected.

---

## 3. Use Case Scenarios

This section outlines the primary user interactions with the application, grouped by intent and context of use. Each base flow describes the ideal full-feature experience when internet access is available. A contextual differences table then highlights how behavior varies depending on whether the user is at home, in the store, or offline.

---

### 3.1 Base Use Case: User Has a Meal or Ingredient in Mind

1. The user launches the app and lands on the homepage.
2. They tap the search bar and enter the name of a meal or ingredient.
3. The app redirects them to a dedicated result screen showing:
   - A short description of the selected item.
   - A representative image.
   - Two columns: one for wine, one for cheese.
   - Each column contains three recommended products with its name, a photo, brief description, and price.
   - One item per column is visually highlighted as the expert-recommended pairing.
4. The user can tap a product to open a detailed page with:
   - Extended description
   - Product origin
   - Tasting notes
   - In-store location
5. Users can save products to their favorites for later access.

---

### 3.2 Base Use Case: User Doesn’t Have a Meal in Mind

1. The user opens the app and lands on the homepage.
2. They are presented with curated recipe categories:
   - Seasonal recipes
   - Regional specialties
   - Trending dishes
   - Low-budget options
3. The user taps a category and scrolls through available recipes.
4. Upon selecting a recipe, they are taken to a screen similar to 3.1 with:
   - A short recipe description and image.
   - Two columns of product suggestions (wine and cheese) with highlighted expert picks.
5. Product detail pages and the ability to save favorites remain available.

---

### 3.3 Base Use Case: User Selects from Favorites

1. The user launches the app and taps the “Favorites” tab in the bottom navigation bar.
2. A list of saved wine and cheese products is displayed.
3. The user can:
   - Tap any product to access full product details (description, origin, tasting notes, in-store location).
   - Remove products from the favorites list if no longer desired.

---

### 3.4 Contextual Differences

| **User Action / Context**                      | **At Home or Outside the Store (Online)**                               | **In Store (Online)**                                                    | **In Store (Offline)**                                                                 |
|------------------------------------------------|-------------------------------------------------------------------------|---------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| **Has a meal or ingredient in mind**           | Full functionality available.                                            | Same as “At Home” with real-time access to in-store product location.     | Limited to preloaded meals. Search restricted to the 100 most popular items.              |
| **Doesn't have a meal in mind**                | Can browse and select from curated recipe categories.                   | Same as “At Home” with product location access.                           | Feature disabled. User must have something in mind or be online.                      |
| **Selects a wine or cheese from favorites**    | Can access, view, and manage favorites with full product details.       | Same as “At Home” with in-store location displayed for each item.         | Can access saved favorites, but only pre-cached product info is available.            |

---

## 4. Functional Requirements  

The core functionality of the application is to recommend wine and cheese pairings based on the user’s selected meal or ingredients. The reverse is intentionally unsupported: users cannot start from a specific wine or cheese and receive a meal suggestion.

Due to offline usage considerations and storage limitations, only a subset of data will be available without an internet connection. Key offline and system behaviors are detailed below.

---

### 4.1 Offline Functionality  

- The application must remain partially functional when offline.
- Only the **100 most popular ingredients** will be stored locally, allowing users to search for and receive recommendations based on these.
- **Wine and cheese** will be stored locally as they are not so many in the store and it won't take too much space to store basic information about them.
- **Favorited products** will be fully accessible offline, including all relevant product data except images.
- **Dietary restrictions and allergy information** are stored locally and applied during offline searches.
- **User preferences** (e.g., budget range, style) are not stored offline and will not influence recommendations when disconnected.
- **Images** will not be displayed in offline mode to minimize app size. Product cards will only show the **name** , **brief description** and **price**.
- Recipe categories such as **seasonal recipes**, **regional specialties**, **trending dishes**, and **low-budget options** will be visible but disabled (greyed out) when offline. Tapping these will trigger a message indicating that the feature is unavailable without internet access.
- The app will display a persistent or temporary **offline notice** informing the user of limited functionality.

---

### 4.2 Favorites System  

- Users can **save any wine or cheese** to their favorites by clicking on the heart icon on wine and cheese pages.
- Favorites are stored locally on the device to ensure offline access.
- Each saved product includes: name, brief description, price, origin, tasting notes, and in-store location (when available).
- Users can access the **Favorites page** from the bottom navigation bar.
- Items can be removed from the favorites list at any time.

---

### 4.3 Navigation Structure  

- The app features a **bottom navigation bar** with tabs for:
  - Homepage
  - Favorites
  - Profile
- Users navigate between:
  - Homepage → Meal input/search
  - Recipe categories (when online)
  - Recommendation screens
  - Product detail pages
  - Favorites list
  - Profile settings
- The app must include smooth, consistent **back navigation** within pages that are not homepage, favorites or profile to return to the previous screen.

---

### 4.4 Search Logic  

- The search bar on the homepage allows users to enter a **meal or ingredient**. When the user starts typing, the app will suggest matching items.
- When a **meal or ingredient** is selected, it redirects to the **meal or ingredient** screen with details and recommendations.
- Only searches for the **100 most popular ingredients** will work offline.
- If no matching ingredient is found (especially offline), the user is shown the following message: **"No results matching your search."**

---

### 4.7 Performance Assumptions  

- The app is expected to load the homepage in under **2 seconds** on a 4G connection.
- Navigating between screens (e.g., homepage → search results → product detail) should be done in under **1 second** to make sure the user doesn't feel like the app is lagging.
- Offline mode should load available cached content instantly, without delay.

---

### 4.8 Localization / Multilingual Support  

- The initial version will be in **French only**, matching the target audience of the Saint-Rémy-de-Provence store. It time allows it, the app will be available in **English** as well.
- The application architecture should allow for easy future translation into other languages (e.g., use of string tables, no hardcoded text).
- The app should automatically detect the device language and display the app in that language if supported. Otherwise, it will default to **French** as long as **English** is not available then, **English** will be the default language.

---

### 4.9 Caching and Data Persistence

- The app will fetch updated product data (e.g., pricing, descriptions, availability) from the database **each time the app is launched**, provided there is an internet connection.
- **User settings** (dietary restrictions, allergies, language preference, and budget range) will be stored **locally** and persist as long as the app remains installed on the device.
- **Search history**:
  - The last **6 user searches** will be stored locally in the cache and displayed on the homepage.
  - These can be overwritten as new searches are performed.
  - There is currently **no manual way to clear search history**, but it will be wiped if the app is uninstalled.

---

### 4.10 First-Time User Experience

---

### 4.11 Error and Empty State Handling

The application must handle errors gracefully and provide clear feedback to users across all states:

- **No Search Results**:
  - Display: `"No results matching your search."`

- **Recipe Category with No Recipes**:
  - Display: `"There are no recipes available in this category at the moment."`

- **Favorites Page Empty**:
  - Display: `"You haven't saved any favorite products yet."`

- **Removed or Unavailable Favorite Product**:
  - If a product previously saved as a favorite is no longer available in the catalog, it should be **automatically removed from the favorites list** during the next data refresh.

- **Missing Product Data**:
  - **Image missing**: Show a placeholder image icon to maintain layout consistency.
  - **Textual data missing** (e.g., name, description, tasting notes): Display placeholder text such as:
    - `"No name available"`
    - `"No description available"`
    - `"No tasting notes available"`

- **Offline Restrictions**:
  - When the user tries to access a feature that is unavailable offline (e.g., curated recipes), show:
    - `"This feature is not available offline. Please connect to the internet to continue."`

---

## 5. Page-by-Page Description

A mockup has been created for each page of the application. The following sections describe the purpose of each page, its components, and the expected user interactions. When it comes to design details, the [mockups](https://www.figma.com/proto/RO0qGCWbS70Pyk50Tr62kS/Intermarche?node-id=1-2&p=f&t=wTVW9SEC38yfSACm-1&scaling=scale-down&content-scaling=fixed&page-id=0%3A1&starting-point-node-id=1%3A2) are the reference. The following sections will only describe the main components and their expected behavior.

Please refer to the [mockups](https://www.figma.com/proto/RO0qGCWbS70Pyk50Tr62kS/Intermarche?node-id=1-2&p=f&t=wTVW9SEC38yfSACm-1&scaling=scale-down&content-scaling=fixed&page-id=0%3A1&starting-point-node-id=1%3A2) for a visual representation of the design and layout.

### 5.1 Navigation Bar
- **Purpose**: The navigation bar provides quick access to the main sections of the app: homepage, favorites, and profile.
- **Components**:
  - Three tabs: homepage, favorites, and profile.
  - Each tab is represented by an icon and a label.
- **Interactions**:
    - Tapping the homepage tab redirects to the homepage.
    - Tapping the favorites tab opens the favorites page.
    - Tapping the profile tab opens the profile settings page.

### 5.2 Homepage

- **Purpose**: The homepage serves as the main entry point for users, providing access to the search bar, recipe categories, and navigation bar.
- **Components**:
  - Search bar: Allows users to enter a meal or ingredient.
  - Recipe categories: Displays curated recipe categories (seasonal, regional, trending, low-budget).
  - Search history: Shows the last 6 searches (stored in the cache) made by the user.
  - Bottom navigation bar: Provides access to the homepage, favorites, and profile.
- **Interactions**:
  - Tapping the search bar allows users to enter a meal or ingredient and when they click on one, it redirects to the meal or ingredient screen.
  - Tapping a recipe category redirects to the corresponding recipe list.
  - Tapping a search history item redirects to the meal or ingredient screen.
  - Tapping the favorites tab opens the favorites page.

### 5.3 Recipe List Screen
- **Purpose**: Displays a list of recipes within a selected category.
- **Components**:
  - Category name: Displays the selected recipe category.
  - Image: Shows a representative image of the category.
  - Back button: Allows users to return to the previous screen.
  - List of recipes: Each recipe includes a photo and its name.
- **Interactions**:
  - Tapping a recipe redirects to the meal or ingredient  screen.
  - Tapping the back button returns to the homepage.

### 5.4 Meal or Ingredient Screen
- **Purpose**: Displays the selected meal or ingredient with recommendations for wine and cheese pairings.
- **Components**:
  - Meal or ingredient name: Displays the selected item.
  - Image: Shows a representative image of the meal or ingredient.
  - Description: Provides a brief description of the meal or ingredient.
  - Back button: Allows users to return to the previous screen.
  - Favorites button: Allows users to save the product to their favorites list.
  - Two columns: One for wine and one for cheese.
  - Three recommended products per column: Each product includes its name, a photo, brief description, and price.
  - Expert-recommended pairing: One item per column is visually highlighted in a soft orange and a label "Our experts recommendation" as the expert-recommended pairing.
- **Interactions**:
  - Tapping a product redirects to the product detail  page.
  - Tapping the back button returns to the previous  screen (homepage or search results).
  - Tapping the favorites icon saves the product to the  favorites list.

### 5.5 Product Detail Page
- **Purpose**: Displays detailed information about a selected wine or cheese product.
- **Components**:
  - Product name: Displays the name of the product.
  - Image: Shows a representative image of the product.
  - Price: Displays the price of the product.
  - Back button: Allows users to return to the previous screen.
  - Favorites button: Allows users to save the product to their favorites list.
  - Description: Provides an extended description of the product.
  - Origin: Displays the origin of the product.
  - Tasting notes: Provides tasting notes for the product.
  - In-store location: Indicates where the product can be found in the store.
- **Interactions**:
  - Tapping the back button returns to the previous  screen (meal or ingredient screen).
  - Tapping the favorites icon saves the product to the  favorites list.

### 5.6 Favorites Page
- **Purpose**: Displays a list of saved wine and cheese products.
- **Components**:
  - Favorites header: Displays the title "My favorites".
  - List of saved products: Each product includes its name, a photo, brief description, and price.
  - Remove button: Allows users to remove a product from the favorites list with a bin icon.
- **Interactions**:
  - Tapping a product redirects to the product detail page.
  - Tapping the remove button removes the product from the favorites list.

### 5.7 Profile Page
- **Purpose**: Displays user profile settings and preferences.
- **Components**:
  - Profile header: Displays the title "My profile".
  - Dietary restrictions: Allows users to select dietary restrictions (e.g., vegetarian, allergies).
  - Allergy list: Displays a list of common allergens (e.g., nuts, gluten) with checkboxes for user selection.
  - Budget range: Allows users to set a budget range for recommendations.
  - Language selection: Allows users to select the app language (French or English).
- **Interactions**:
  - Tapping the dietary restrictions or allergy list allows users to select or deselect options.
  - Tapping the budget range allows users to set a minimum and maximum price.
  - Tapping the language selection allows users to choose between French and English.

