App file responsibilities
=========================

- UI entry and app initialisation (``lib/main.dart``)
   
   - Feature screens:

      - ``lib/views/categories.dart``
      - ``lib/views/shopping_list_screen.dart``
      - ``lib/views/recipe_page.dart``
   - Models:

      - ``lib/models/recipe.dart``
      - ``lib/models/ingredient.dart``
      - ``lib/models/category.dart``
      - ``lib/models/shopping_list_item.dart``
   - Data access:

      - ``lib/services/database_service.dart``
      - ``lib/services/category_service.dart``
   - Graph logic:

      - ``lib/graph_controller.dart``
      - ``lib/graph_widget.dart``
   - Styling:

      - ``lib/views/app_styles.dart``
   - Tests:

      - ``test/``