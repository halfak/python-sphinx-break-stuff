.. sphinx_test documentation master file, created by
   sphinx-quickstart on Mon Jan 11 19:34:53 2016.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to sphinx_test's documentation!
=======================================
This documentation represents a test of a weird bug in sphinx.  These HTML
files were generated against a python module with the following structure:

* sphinx_test/
    * module/
        * submodule/
            * imports_nothing.py
            * imports_base_module.py
            * imports_break_stuff.py **(broken)**
        * imports_nothing.py
        * imports_base_module.py
        * imports_break_stuff.py
    * base_module.py
    * do_things/
        * break_stuff.py

Note that "sphinx_text/module/submodule/imports_break_stuff.py" is marked as **(broken)**.  This is because a strange behavior that happens in sphinx.  See the documentation below that was generated from this module tree.  Note that all of the "Module level" doucumentation is rendered correctly.  However the last pair of instance/class document simply repeats the class's docstring and does not document the attributes.


Module level
------------
Works great!

.. autodata:: sphinx_test.module.imports_nothing
.. autodata:: sphinx_test.module.imports_base_module
.. autodata:: sphinx_test.module.imports_break_stuff

.. autoclass:: sphinx_test.module.ImportsNothing
    :members:
    :member-order: bysource

.. autoclass:: sphinx_test.module.ImportsBaseModule
    :members:
    :member-order: bysource

.. autoclass:: sphinx_test.module.ImportsBreakStuff
    :members:
    :member-order: bysource

Submodule level
---------------
The last one is weird and broken.

.. autodata:: sphinx_test.module.submodule.imports_nothing
.. autodata:: sphinx_test.module.submodule.imports_base_module
.. autodata:: sphinx_test.module.submodule.imports_break_stuff

.. autoclass:: sphinx_test.module.submodule.ImportsNothing
    :members:
    :member-order: bysource

.. autoclass:: sphinx_test.module.submodule.ImportsBaseModule
    :members:
    :member-order: bysource

.. autoclass:: sphinx_test.module.submodule.ImportsBreakStuff
    :members:
    :member-order: bysource


Contents:

.. toctree::
   :maxdepth: 2



Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`
