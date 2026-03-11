Welcome to Lumache's documentation!
===================================

**Lumache** (/lu'make/) is a Python library for cooks and food lovers
that creates recipes mixing random ingredients.
It pulls data from the `Open Food Facts database <https://world.openfoodfacts.org/>`_
and offers a *simple* and *intuitive* API.

Check out the :doc:`usage` section for further information, including
how to :ref:`installation` the project.

.. note::

    This project is under active development.

Documentation plan
------------------

- Project overview and goals
- Setup and run instructions
- App file responsibilities:

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

- Data model and storage flow:

   - How data moves throughout the application:

      - User opens a screen
      - Screen requests a service
      - Service loads saved structures and data models
      - Data is placed back onto the UI

- Feature walkthrough:

   - Optimize shopping list
   - View recipes
   - Add to shopping list

- Testing strategies and current coverage
- Known limitations and future improvements

Contents
--------

.. toctree::

   usage
   api
