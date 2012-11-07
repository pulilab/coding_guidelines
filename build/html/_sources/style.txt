Style Guide
============

.. note:: Our style guide is based on `Mozilla's <http://mozweb.readthedocs.org/en/latest/js-style.html>`_, `Bracket's <https://github.com/adobe/brackets/wiki/Brackets-Coding-Conventions>`_ and `Pocoo's <http://www.pocoo.org/internal/styleguide/>`_ guides.

HTML
-----

Classes and id's in HTML use all lower-case with dashes (-), not camelCase or under_scores:

Do this:

.. code-block:: html

    <div id="search-results">
    <span class="title-wrapper">

Not this:

.. code-block:: html

    <div id="searchResults">  // Don't use camel-case for ids
    <span class="title_wrapper"> // Don't use underscore

Always use double quotes (") to border attributes.

Do this:

.. code-block:: html

    <div id="searchResults">

Not this:

.. code-block:: html

    <div id='searchResults'>

Javascript
-----------

* Use 4 space indents (spaces, no tabs)
* Must pass JSLint. Meaningful defaults for JSLint is

    .. code-block:: javascript

        /*jslint vars: true, plusplus: true, devel: true, nomen: true, indent: 4, maxerr: 50 */
        /*global $ */

    .. note:: The above recommendation has one caveat.

        JSLint warns about lines consisting entirely of whitespace, but we ignore those warnings. The JSLint feature built into Brackets filters out these warnings automatically.

    .. note:: JSHint instead? we might configure it with a single .jshintrc file
* Line length
    **79** characters with a soft limit of 84 if absolutely necessary. Try to avoid too deeply nested code by cleverly placing break, continue and return statements.
* General Naming and Syntax

    Variable and function names use camelCase (not under_scores):

    Do this:
    
    .. code-block:: javascript

        var editorHolder; 
        function getText();
        
    Not this:
    
    .. code-block:: javascript

        var editor_holder; // Don't use underscore!
        function get_text(); // Don't use underscore!

    Never assign multiple variables on the same line.

    Don't do this:

    .. code-block:: javascript

        var a = 1, b = 'foo', c = 'wtf';
* Private variables

    Use _ prefixes on private variables/methods:
    Do this:

    .. code-block:: javascript

        var _privateVar = 42;
        function _privateFunction() 
    
    Not this:
    
    .. code-block:: javascript

        var privateVar = 42; // Private vars should start with _
        function privateFunction() // Private functions should start with _
* Arrays and Objects

    Use `[]` to assign a new array, not `new Array()`.

    Use `{}` for new objects, as well.

    Two scenarios for `[]` (one can be on the same line, with discretion and the other not so much):

    .. code-block:: javascript

        // Okay on a single line
        var stuff = [1, 2, 3];

        // Never on a single line, multiple only
        var longerStuff = [
            'some longer stuff',
            'other longer stuff'
        ];

* Working with jQuery

    Use `$` prefixes on variables referring to jQuery objects:

    Do this:
    
    .. code-block:: javascript

        var $sidebar = $("#sidebar");
    
    Not this:

    .. code-block:: javascript

        var sidebar = $("#sidebar"); // Use '$' to prefix variables referring to jQuery objects

* Use semicolons:
    Do this:

    .. code-block:: javascript
        
        var someVar;
        someVar = 2 + 2;

    Not this:

    .. code-block:: javascript
        
        var someVar   // Missing semicolon!
        someVar = 2 + 2   // Missing semicolon!
* Operators
    Always use `===` for comparison. The only exceptions are when testing for `null` and `undefined`

    .. code-block:: javascript

        if (value !== 0) {
            console.log('value can not be undefined');
        }

    Try to avoid ternary, especially if it would use multiple lines:

    This is OK:

    .. code-block:: javascript

        return user.isLoggedIn ? 'yay' : 'boo';

    Not this:

    .. code-block:: javascript

        var foo = (user.lastLogin > new Date().getTime() - 16000) ? user.lastLogin - 24000 : 'wut';

* Quoting
    Use double quotes in JavaScript. If a JavaScript string literal contains code within it, use single quotes within the string to avoid escaping.

    Do this:

    .. code-block:: javascript
        
        var aString = "Hello";
        someFunction("This is awesome!");

        var htmlCode = "<div id='some-id' class='some-class'></div>";

    Not this:

    .. code-block:: javascript

        var aString = 'Hello'; // Use double quotes!
        someFunction('This is awesome!'); // Use double quotes!

        var htmlCode = '<div id="some-id" class="some-class"></div>'; // Use double quotes!
        var htmlCode = "<div id=\"some-id\" class=\"some-class\"></div>"; // Within string, use single quotes!

* Commenting
    All comments should be C++ single line style 

    .. code-block:: javascript
        
        //comment.

    Even multiline comments should use // at the start of each line

    Use C style `/* comments */` for notices at the top and bottom of the file

    Annotations should use the `/** annotation */` style

    .. code-block:: javascript

        /** This is my function

        @param arg1 string The first argument
        @return boolean
        */
        var myFunc = function (arg1) {
            return true;
        };

    Annotate all functions

CSS
----

Use Less_

.. _Less: http://lesscss.org/

Python
-------

Use the `Pocoo style guide <http://www.pocoo.org/internal/styleguide/>`_

In addition:

* Lint/PEP-8 compliance (Use `Pylint <http://pypi.python.org/pypi/pylint>`_)
