====================
django-view-permission
====================

View permissions to Django admin

Installation
------------

1. This library is on PyPI so you can install it with:

.. code-block:: bash

    pip install django-view-permission

or from github:

.. code-block:: bash

    pip install git+https://github.com/PetrDlouhy/django-view-permission#egg=django-view-permission

2. Add ``view_permission`` to your ``INSTALLED_APPS`` setting like this:

.. code-block:: python

    INSTALLED_APPS = (
        ...
        'view_permission',
    )

Usage
-----

Just use it the mixin:

.. code-block:: python

   from view_permission.admin import ViewPermissionMixin

   class FooAdmin(ViewPermissionMixin, admin.ModelAdmin):
      ...

