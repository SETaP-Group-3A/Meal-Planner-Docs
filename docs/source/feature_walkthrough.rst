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