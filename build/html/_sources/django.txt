Django Guidelines
==================

Project skeletons
-----------------

The recommended project skeleton to be used for django projects can be found in `our django-skel2`_ repo.

.. _`our django-skel2`: https://github.com/pulilab/django-skel2

.. note:: Requires django 1.4 for project creation.

The following commands will start a new project with some feature-rich settings in `YOUR_PROJECT_NAME` directory. 

For normal django projects
___________________________

To use it simply run the following command when starting a new project:

.. code-block:: bash

	django-admin.py startproject --template https://github.com/pulilab/django-skel2/zipball/pulilab --extension py,md,ini YOUR_PROJECT_NAME

For appengine projects
_______________________

To be developed.

Structure
----------

.. warning:: Likely, as time goes by, some other programmers will have to read and understand your code. As a result, try to follow these guidelines as well as you can!

Testing
--------

Deployment
-----------

Use fabric. There are pre-written fabric script in our project templates.

Blogs to follow
----------------

* `The django community aggregator <http://www.djangoproject.com/rss/community/>`_
* `Our collection of django related links <http://groups.diigo.com/group/pulilab/content/tag/django>`_
* `Djangopackages' RSS feed <http://www.djangopackages.com/feeds/packages/latest/rss/>`_