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
      - ShoppingList retrieves recipe ingredients from the database
      - For each ingredient, the system selects the best variant (by cost/distance/calories)
      - Duplicate ingredients are combined with aggregated quantities
      - Sorted list is displayed in ShoppingListScreen based on the user's preference
      - Changes to quantities sync to the database

Location service data flow
-----------------------

How location data is calculated and used:

      - User inputs a valid postcode address and opts in to the location
      - Address is passed to the location service to calculate the distance to nearby stores
      - User's location is passed to an API to calculate longitude and latitude
      - User's location and each ingredient's store location are passed to haversine formulat to calculate distance
      - Distance to each ingredient is updated and displayed on future shopping lists

Page style data flow
--------------------

How the app handles stylistic choices:

      - app_styles stores all static style features
      - Font sizes are set when the app is created
      - Special text features are called statically as type TextStyle

Category data flow
------------------
How category data is displayed and generated:

      - User opens categories page
      - Categories retrieve recipes from the database
      - System, organises and displays these categories, and retrieves nutritional information
      - Nutritional information is displayed for the recipe
      - User favourites a recipe
      - Recipe id is then stored in the user's preferred recipes within the database

Favourite category data flow
----------------------------
How the favourite category data is displayed and generated:

      - User opens favourites category
      - Categories retrieves the user's preferred recipes from the database
      - System, organises and displays these categories, and retrieves nutritional information
      - Nutritional information is displayed for the recipe

Custom recipe creation data flow
--------------------------------

How a user-defined recipe is created and stored:

      - User opens the add recipe screen
      - AddRecipeScreen presents input fields for name, ingredients, quantities, and nutritional            values
      - User fills in recipe details and confirms
      - Screen converts raw input into a Recipe model and associated Ingredient models
      - DatabaseService persists the new recipe and its ingredients to SQLite
      - User is returned to the categories view where the new recipe appears

Goal diary data flow
--------------------

How goal progress is tracked and updated:

      - User opens the goal diary screen
      - GoalDiaryScreen calls GoalRepository to load the current week's WeeklyGoals from the                database
      - Goals mapped to each day of the week are rendered as interactive progress indicators
      - User logs progress or marks a goal complete
      - GoalRepository writes the updated state back to the database
      - Screen refreshes to reflect the new totals and streaks

Log in data flow
----------------
How the user enters the application:

      - User opens application
      - Application shows input fields for entering email and password
      - User enters own email
      - User enters own password
      - User presses "Log In"
      - Application retrieves user credentials from the database and checks the validation
      - Application opens on the user's specified account or displays an error message if incorrect

Account creation data flow
--------------------------
How the user creates an account:

      - User opens Account Creation page
      - Application shows input fields for entering email, entering password and confirming password
      - User inputs new email
      - User inputs new password
      - User repeats new password
      - User presses "Create Account"
      - Application validates credentials and either stores new information in the database or displays an error message if incorrect
      - Application opens log in page for the user to enter credentials
