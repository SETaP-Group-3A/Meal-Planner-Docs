App file responsibilities
=========================

- UI entry and app initialisation (``lib/main.dart``)
   
   - Feature screens:

      - ``lib/views/categories.dart``
      - ``lib/views/shopping_list_screen.dart`` — Displays shopping list with sorting and quantity             management
      - ``lib/views/recipe_page.dart`` — Handles dynamic serving size calculations, local state for           ingredient exclusion, and advanced nutritional views.
      - ``lib/views/add_recipe_screen.dart`` — Manages UI state and data conversion for custom                recipe creation and SQLite persistence routing.
      - ``lib/views/category_content_screen.dart`` — Displays the contents and specific recipes               saved within an individual category folder.
      - ``lib/views/goal_diary_screen.dart`` — Interactive UI for users to track and update their             daily/weekly progress against their goals.
      - ``lib/views/settings_screen.dart`` — Manages user preferences, including dark mode toggles,           accessibility, and primary goal selection.
      - ``lib/views/store_locator_screen.dart`` — Displays nearby store options based on distance             calculations and user postcode.

   - Models:

      - ``lib/models/recipe.dart``
      - ``lib/models/ingredient.dart``
      - ``lib/models/category.dart``
      - ``lib/models/shopping_list_item.dart`` — Represents an ingredient with its quantity
      - ``lib/models/store.dart``
      - ``lib/models/weekly_goals.dart`` — Data structure representing user goals mapped to                   specific days of the week.

   - Data access:

      - ``lib/services/database_service.dart`` — Database connection for the whole application
      - ``lib/services/category_service.dart``
      - ``lib/services/location_service.dart`` — Distance calculation using haversine and geocoding
      - ``lib/repositories/goal_repository.dart`` — Handles database querying and updates for the             weekly goal tracker.

   - Shopping list logic:

      - ``lib/shopping_list.dart`` — Managing in-memory shopping list, ingredient aggregation, and            sorting

   - Graph logic:

      - ``lib/graph_controller.dart``
      - ``lib/graph_widget.dart``

   - Styling:

      - ``lib/views/app_styles.dart``

   - Utils

      - ``lib/utils/haversine.dart`` — Distance calculation whilst preventing circular dependency

   - Tests:

      - ``test/``

   - Log in logic:

      - ``lib/views/log_in.dart`` - Managing user credential entry

   - Account creation logic:

      - ``lib/views/sign_up.dart`` - Managing user account creation credential entry
