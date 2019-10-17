# Software Must Be Installable with `python setup.py install`

This is one of the tier 1 standards. See full list [on the overview page](tier1_standards_overview.md).

## Short description
The command `python setup.py install` (or `python setup.py develop`) will build and install all of the modules in the software repository. In order for this command to work, the software repository must have a `setup.py` file and resemble that of a package structure.

## Importance of this standard
Allowing the software repository to be installable via `setup.py` enables users as well as external tools and services (e.g. `Jenkins`, `Travis`, `ReadtheDocs`, etc.) to simply and easily install the software in an appropriate software environment.  Furthermore, the use of a `setup.py` module allows developers to set package installation requirement parameters and metadata, resulting in a simple command to be used on the part of the end user.  If the software repository is organized as a python package, users will be able to import the software into a python environment with `import package_name`.

## Options for this standard
There is only one option for complying with this standard for Python, which is described below. If the software is in a language other than Python, you will need to research how to setup an installation process such that it meets the ease-of-use standards described in the above section.

## How to apply this standard
- The software must be organized in a package-like structure. See the [STScI Style Guide on Python Packaging](https://github.com/spacetelescope/style-guides/blob/master/guides/python-package.md) for further details.
- You must have a `setup.py` file in the top level of the software repository. See [Python's setup.py example](https://packaging.python.org/tutorials/packaging-projects/#creating-setup-py) for more information on what to include in this file. Also see the example listed under the "Useful Links" section below.

You can check that your module/package is installed correctly by running `python setup.py install` in the outer-most level of your package, and then importing it with `import package_name`.

## Useful Links
- An [STScI template GitHub repository](https://github.com/spacetelescope/stsci-package-template) which shows a more complex example of `setup.py` including calling a `setup.cfg` file
