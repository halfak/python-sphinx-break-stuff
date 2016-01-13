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

Note that "sphinx_text/module/submodule/imports_break_stuff.py" is marked
as **(broken)**.  This is because a strange behavior that happens in
sphinx.  To generate the documentation:

1. Clone this repository
2. Run `$ make html` inside the *doc/* directory
3. Open *doc/_build/sphinx_test/doc/_build/html/index.html* in your browser

Note that all of the "Module level" doucumentation is rendered
correctly.  However the last pair of "Submodule level" instance/class 
documentation simply repeats the class's docstring and does not document the
attributes.  This is apparently related to the import of
*do_thing/break_stuff.py* from *module/submodule/imports_break_stuff.py*.
