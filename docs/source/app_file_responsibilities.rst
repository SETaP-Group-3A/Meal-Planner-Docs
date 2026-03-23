App file responsibilities
=========================

- UI entry and app initialisation (``lib/main.dart``)
   
   - Feature screens:

      - ``lib/views/categories.dart``
      - ``lib/views/shopping_list_screen.dart`` — Displays shopping list with sorting and quantity management
      - ``lib/views/recipe_page.dart``
   - Models:

      - ``lib/models/recipe.dart``
      - ``lib/models/ingredient.dart``
      - ``lib/models/category.dart``
      - ``lib/models/shopping_list_item.dart`` — Represents an ingredient with its quantity
   - Data access:

      - ``lib/services/database_service.dart`` — Database connection for the whole application
      - ``lib/services/category_service.dart``
   - Shopping list logic:

      - ``lib/shopping_list.dart`` — Managing in-memory shopping list, ingredient aggregation, and sorting
   - Graph logic:

      - ``lib/graph_controller.dart``
      - ``lib/graph_widget.dart``
   - Styling:

      - ``lib/views/app_styles.dart``
   - Tests:

      - ``test/``