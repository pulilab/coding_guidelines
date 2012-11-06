Web Frontend Guidelines
========================

Frontend Tooling
-------------------

We recommend using `lineman`_

.. _lineman: https://github.com/pulilab/lineman

It offers several handy features for front-end development:

* Browser auto-reloading on file changes
* Immediately compile CoffeeScript, Less_, and client-side templates as you edit source files
* Provide a development server for fast feedback
* Concatenate & minify all your CSS & JavaScript for production
* Run specs on demand with `lineman spec` using Testem_
* Run specs with output suitable for your CI server using `lineman spec-ci`

.. _Less: http://lesscss.org/
.. _Testem: https://github.com/airportyh/testem

Installation
_____________

.. code-block:: bash

	npm install -g https://github.com/pulilab/lineman/zipball/master

This installs the `lineman` command.

For browser auto-reloading, you should install a `livereload extension`_

.. _`livereload extension`: http://feedback.livereload.com/knowledgebase/articles/86242-how-do-i-install-and-use-the-browser-extensions

Usage
______

To start a new project

.. code-block:: bash

	lineman new <project_name>

This generates our preferred directory structure in the `app` directory.

To serve it for your browser run

.. code-block:: bash

	lineman run

To run your tests run

.. code-block:: bash

	lineman spec

Handlebar templates
^^^^^^^^^^^^^^^^^^^^^

Lineman supports underscore_ and handlebars_ templates. Handlebars templates should have one of the following file extensions:

* .hb
* .handlebar
* .handlebars

.. _underscore: http://underscorejs.org/
.. _handlebars: http://handlebarsjs.com/

Troubleshooting
________________

The generated and served files are in the `generated` directory. If you have some mysterious problem, you should check out the generated files first.

Javascript libraries
---------------------

We recommend using one of the following JS frameworks:

* Backbone_ with Marionette_, Relational_ etc
* Ember_

.. _Backbone: http://backbonejs.org/
.. _Marionette: http://marionettejs.com/
.. _Relational: https://github.com/PaulUithol/Backbone-relational
.. _Ember: https://github.com/PaulUithol/Backbone-relational

Moreover, we have `a continuously growing collection of articles to read <http://groups.diigo.com/group/pulilab/content/tag/javascript>`_.