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