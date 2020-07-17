# Software Must Use Python>=3.6 Where Applicable

This is one of the tier 2 standards. See full list [on the overview page](README.md).


## Short description

We require that all Python software 'support' python version 3.6 or higher.  We define 'support' in this context such that:

- The python software is fully operational with no errors when invoked from an interpreter that uses Python 3.6 or higher,
- Any future contributions to the software must also adhere to the above requirement
- Any provided environment file(s) in the repository (i.e. `environment.yml`, `requirements.txt`, `setup.py`), must all list a consistent version of python.
- Any defined software environments within continuous integration builds (i.e. Jenkins or Travis) must be using the supported python version(s)


## Importance of this standard

With python being an free, open-source language, the python community continues to build and improve the existing language, resulting in periodic releases of new versions of the python native library as well as many third-party libraries that we commonly use at STScI (e.g. `bokeh`, `astropy`, `numpy`, etc.).  As such, over time the python software that we write becomes outdated, and the versions of the dependencies that we rely on become unsupported.  This in turn makes it difficult for future developers to maintain existing software and their environments as well as build new features.  For these reasons, we make an effort to keep our software operational with newer python versions, as does the python community as a whole, in order to avoid some of these future issues.

Currently, many of the python libraries we use support python versions 3.6, 3.7, and/or 3.8.  As such, we are requiring teams to support at least python version 3.6.


## How to apply this standard

For software that must be upgraded from Python 2.x to Python 3.x, the tool [`2to3`](https://docs.python.org/2/library/2to3.html) can be used to show (and optionally apply) all of the necessary changes.  For a general description of what aspects of the Python 2.x code must be changed in order to comply with Python 3.x, see the [official Python documentation on 'updating your code'](https://docs.python.org/3/howto/pyporting.html#update-your-code).

For software that must be upgraded from Python<=3.5 to Python>=3.6, unfortunately an automated tool akin to `2to3` does not exist for showing what could be upgraded in your software.  The best way to see what is different between python 3 versions is to consult the [official python "whats new" documentation](https://docs.python.org/3.8/whatsnew/).  Furthermore, teams may modify their Jenkins and/or Travis environments to run automated tests in an upgraded python environment and make sure that tests are passing.

In addition to upgrading any python software, teams must also ensure that the python version used in provided software environments are all consistent.  This includes conda environments (i.e. `environment.yml`), package environments (i.e. `requirements.txt`, `setup.py`, sphinx documentation), and continuous integration environments (i.e. Jenkins or Travis configuration files).  Make sure to update any of these files as necessary.


## Useful Links

- [`2to3`](https://docs.python.org/2/library/2to3.html)
- [Porting python 2 software to python 3](https://docs.python.org/3/howto/pyporting.html#update-your-code)
- [What's new in python versions](https://docs.python.org/3.8/whatsnew/)
