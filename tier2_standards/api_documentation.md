# Software Must Document Modules, Classes, and/or Functions

This is one of the tier 2 standards. See full list [on the overview page](README.md).

## Short description

One of the key aspects of documenting code, is documenting how users should expect to interact with different modules, classes, methods, and/or functions that live in your code. The common way of documenting these objects is to use documentation strings or "docstrings", which are string literals that give an overview of the object it's describing.

## Importance of this standard

Docstrings for the modules, classes, and/or functions in your code serve a variety of purposes. They:
- Act as formalized, proper documentation
- Allow users to better understand how the software works and how to use it
- Improve the overall readability of code and decrease on-boarding time for new developers
- Can be more easily accessed than other kinds of comments due to their formatting, either through the `help()` function, `__doc__` attribute, or by being ported to online documentation

## Options for this standard

Python has a style guide specifically for docstrings called [`PEP257`](https://www.python.org/dev/peps/pep-0257/) (where PEP stands for Python Enhancement Proposal). `PEP-257` gives an overview of what docstrings are and how they should be formatted.

There is also a more in-depth document on formatting docstrings called [NumpyDocs](https://numpydoc.readthedocs.io/en/latest/format.html). This is the formatting recommended by the [STScI Style Guide](https://github.com/spacetelescope/style-guides/blob/master/guides/python.md#docstrings).

No matter the formatting, there are certain pieces of information that should be included in docstrings:
- A brief overview of what the object is/does
- Information on inputs to the object including the names of parameters, their types, and a description
- Information on what the object returns, if anything, including their types and a description

There is also some optional information that can be included, like:
- Examples
- Notes
- References

Furthermore, module docstrings should contain:
- An overview of what the module is/does
- A list of authors that have contributed to the module
- A "use" section that describes how a user may import and/or execute the module.

For other information that can be included in docstrings, see these [examples from NumpyDocs](https://numpydoc.readthedocs.io/en/latest/format.html#sections).

## How to apply this standard

All of the modules, functions, classes, and/or methods in your code base should be accompanied by a docstring.

If docstrings already exist in your code base, we will not force you to change the formatting, only to make sure that the formatting is self-consistent and all of the information discussed above is included when relevant. If you are adding docstrings for the first time, we highly recommend you follow the NumpyDocs and `PEP257` style.

If developers feel it is appropriate, they may want to make the docstrings easier to find for users by compiling and placing them in their main documentation. This can be done using [Sphinx](https://www.sphinx-doc.org/en/master/index.html) to build their documentation and using one of the following plugins to automatically include the docstrings:

- [Automodapi](https://sphinx-automodapi.readthedocs.io/en/latest/)
- [Autodoc](https://www.sphinx-doc.org/en/master/usage/extensions/autodoc.html)
- [NumpyDoc](https://numpydoc.readthedocs.io/en/latest/install.html)
