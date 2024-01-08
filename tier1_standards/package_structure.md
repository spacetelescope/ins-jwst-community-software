# Software Must Be Installable with `pip install .`

This is one of the tier 1 standards. See full list [on the main page](../README.md).

## Short description
The command `pip install .` (or `pip install -e .`) will build and install all of the modules in the software repository. In order for this command to work, the software repository must have a pyproject.toml file and resemble that of a package structure.

## Importance of this standard
Allowing the software repository to be installable via `pip install .` enables users as well as external tools and services (e.g. `ReadtheDocs`, etc.) to simply and easily install the software in an appropriate software environment.  Furthermore, the use of a `pyproject.toml` module allows developers to set package installation requirement parameters and metadata, resulting in a simple command to be used on the part of the end user.  If the software repository is organized as a python package, users will be able to import the software into a python environment with `import package_name`.

## Options for this standard
There is only one option for complying with this standard for Python, which is described below. If the software is in a language other than Python, you will need to research how to setup an installation process such that it meets the ease-of-use standards described in the above section.

## How to apply this standard
- The software must be organized in a package-like structure. See the [STScI Style Guide on Python Packaging](https://github.com/spacetelescope/style-guides/blob/master/guides/python-package.md) for further details.
- You must have a `pyproject.toml` file in the top level of the software repository. See [Python's tutorial example](https://packaging.python.org/en/latest/tutorials/packaging-projects/#creating-the-package-files) for more information on what to include in this file. Also see the example listed under the "Useful Links" section below.

You can check that your module/package is installed correctly by running `pip install .` in the outer-most level of your package, and then importing it with `import package_name`.

## Useful Links
- An [STScI template GitHub repository](https://github.com/spacetelescope/stsci-package-template) which shows another example of `pyproject.toml`
