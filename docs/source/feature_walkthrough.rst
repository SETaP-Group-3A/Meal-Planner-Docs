Feature walkthrough
===================

Add to shopping list
--------------------

   1. User selects a recipe
   2. ShoppingList processes each recipe and extracts its required ingredients
   3. Duplicate ingredients from multiple recipes are aggregated
   4. The system automatically selects the best ingredient variant based on selected goals
   5. Aggregated shopping list is displayed in ShoppingListScreen
   6. Data is persisted to the database

Optimize shopping list
----------------------

   - User can sort the shopping list by three goals:

      - **Cost** — Prioritizes cheapest ingredients
      - **Distance** — Prioritizes closest store locations
      - **Calories** — Prioritizes healthiest (lowest calorie) options
   - Quantities can be adjusted per item
   - Selected items can be marked when shopping

Display Graph
-------------

   1. User enters app
   2. Determine the currently active user goal
   3. GraphController creates list of this weeks values by iterating through last 7 days
   4. GraphWidget populates axis
      - **x**: day of the week
      - **y**: score for that day


Update Graph Display
--------------------

   1. User enters diary
   2. User edits a goal
   3. On return to homepage, graph is rebuilt with new values

Calculate Weekly Total
------------

   1. User enters diary
   2. WeeklyGoal finds this weeks goals
   3. GoalRepository adds all values for this week

Calculate Weekly Comparison
-----------------

   1. User enters diary
   2. WeeklyGoal finds this weeks goals
   3. Then find last weeks goals
   4. GoalRepository subtracts this weeks value from last week

Settings Page
-----------------

   1. User opens the Settings screen and chooses between Account or Accessibility
   2. Account Settings loads previously saved details and fills in the form automatically
   3. User updates their information and submits the form, with checks to make sure everything is valid
   4. The app saves the updated details locally, only keeping the address if the user hasn’t opted out
   5. If the user chooses not to provide an address, the field is disabled, cleared, and no longer required
   6. Accessibility Settings shows the current theme and updates automatically when it changes
   7. User can switch Dark Mode on or off, and the app immediately applies and saves the preference
   8. When the app starts, it remembers the user’s theme choice and applies it across the app