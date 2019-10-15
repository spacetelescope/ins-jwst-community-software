# Software Must Be Available With Conda or Pip

This is one of the tier 1 software standards. See full list [here](tier1_standards_overview.md)

## Short description
While your users can download your software files and install your package with `python setup.py install` as described [here](package_structure.md), it is also possible to distribute your software with by uploading it to package manager. This can turn your package installation process to single lines like `pip install <package>` and `conda install <package>`.

## Importance of standard
While packaging your software and having it available as an open source repository is a good way to let your users access it, it can be made even easier by allowing your package to be installable with either pip or conda. Your user will be able to use a single line installation without needing prior knowledge of software.

## Options for this standard
- PyPi (the Python Package Index; this must be a Python package)
- Conda via Astroconda (not language dependent)
- Conda via Conda-Forge (not language dependent)

## How to apply this standard
First, you package setup must be complete such that your package:
- Is installable with `python setup.py`. See [here](package_structure.md) for instructions
- Has a license file. See [here](license_file.md) for instructions
- Has a README file

To add your package to PyPi:
- See these [instructions from Python](https://packaging.python.org/tutorials/packaging-projects/#generating-distribution-archives)
- Note that these tell you to upload your package to Test PyPi as a check before uploading it to PyPi. We agree and recommend you install your package from Test PyPi and run your tests locally before determining if you're ready to upload to PyPi.

To add your package to Astroconda:
- See their [contributing guide](https://astroconda.readthedocs.io/en/latest/contributing.html#adding-a-recipe-to-astroconda-contrib)

To add your package to Conda-Forge:
- See their [contributing guide](https://conda-forge.org/docs/maintainer/adding_pkgs.html#contributing-packages)

## Useful Links
- [Installing a package from Pip](https://packaging.python.org/tutorials/installing-packages/)
- [Installing a package from Astroconda](https://astroconda.readthedocs.io/en/latest/index.html)
- [Installing a package from Conda-Forge](https://conda-forge.org/docs/user/introduction.html#how-can-i-install-packages-from-conda-forge) 