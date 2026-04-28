Data model and storage flow
===========================

General data flow
-----------------

How data moves throughout the application:

      - User opens a screen
      - Screen requests a service
      - Service loads saved structures and data models
      - Data is placed back onto the UI

Shopping list data flow
-----------------------

How shopping list data is generated and displayed:

      - User adds recipe to shopping list
      - ShoppingList retrieves recipe ingredients from database
      - For each ingredient, the system selects best variant (by cost/distance/calories)
      - Duplicate ingredients are combined with aggregated quantities
      - Sorted list is displayed in ShoppingListScreen based on the user's preference
      - Changes to quantities sync to database

Page style data flow
--------------------

How app handles stylistic choices:

      - app_styles stores all static style features
      - Font sizes are set when the app is created
      - Special text features called statically as type TextStyle

Category data flow
------------------
How categories data is displayed and generated:

      - User opens categories page
      - Categories retrieves recipes from database
      - System, organises and displays these categories, and retrieves nutritional information
      - Nutritional information is displayed for the recipe
      - User favourites a recipe
      - Recipe id is then stored in the user's preferred recipes within the database

Favourite category data flow
----------------------------
How favourite category data is displayed and generated:

      - User opens favourites category
      - Categories retrieves the user's preferred recipes from database
      - System, organises and displays these categories, and retrieves nutritional information
      - Nutritional information is displayed for the recipe
