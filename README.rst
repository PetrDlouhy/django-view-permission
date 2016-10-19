====================
django-view-permission
====================

Experimental implementation of view permissions to Django admin.

This application experiment to impement view permissions as stand alone application. Then I decided, that it would be simpler and more effective to achieve this by submitting patch to Django itself. My (and others) effort on this field resulted in Django patch, that can be found at https://code.djangoproject.com/ticket/8936 and https://github.com/django/django/pull/6734

This code probably doesn't work, but can be used as inspiration for rewriting Django patch to standalone application prior it is submited to upstream Django.

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

