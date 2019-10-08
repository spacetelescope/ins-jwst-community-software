# Software Must Be Installable With `python setup.py install`

This is one of the tier 1 software standards. See full list [here](tier1_standards_overview.md)

## Short description
The command `python setup.py install` will build and install all the modules in your software. In order for this command to work, your software must have a `setup.py` file.

## Importance of standard
Allowing users to have a single line option for installing your software improves their chances of correctly installing your software. This is because you can set things like package installation requirements inside your `setup.py` file, allowing for a simple command on the part of the user.

It also allows for an easier interaction between your user and your code base, since your user can import your module or package with the same `import package_name` command from any location on their computer.

## Options for this standard
There is only one option for complying with this standard for Python, which is described below. If your module/package is in a language other than Python, you will need to research how to setup an installation process such that it meets the ease-of-use standards described in the above section.

## How to apply this standard
- All your code must be located in a central directory, the name of which will be what you use for importing.
- You must have a `setup.py` file under your central directory. See [Python's setup.py example](https://packaging.python.org/tutorials/packaging-projects/#creating-setup-py) for more information on what to include in this file. Also see the example listed under the "Useful Links" section below.

You can check that your module/package is installed correctly by running `python setup.py install` in the outer-most level of your package, and then importing it with `import package_name`.

## Useful Links
- An [STScI template GitHub repository](https://github.com/spacetelescope/stsci-package-template) which shows a more complex example of `setup.py` including calling a `setup.cfg` file
