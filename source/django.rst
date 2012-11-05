Django Guidelines
==================

Project skeleton
-----------------

The recommended project skeleton to be used for django projects can be found in `our django-skel2`_ repo.

.. _`our django-skel2`: https://github.com/pulilab/django-skel2

To use it simply run the following command when starting a new project:

.. code-block:: bash

	django-admin.py startproject --template https://github.com/pulilab/django-skel2/zipball/pulilab --extension py,md,ini YOUR_PROJECT_NAME

This will start a new project with some feature-rich settings in `YOUR_PROJECT_NAME` directory. 

.. note:: Requires django 1.4 for project creation.