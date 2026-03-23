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