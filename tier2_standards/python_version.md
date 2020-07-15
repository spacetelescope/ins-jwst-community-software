# Software Must Use Python>=3.6 Where Applicable

This is one of the tier 2 standards. See full list [on the overview page](README.md).

- We will check which python versions each project is using:

jwst_backgrounds - Travis file indicates 3.7, otherwise it is unclear
jwst_gtvt - setup.py indicates <= 3.7, but travis is testing 3.6
jwst_coronograph_visibiltiy - Travis and setup.py indicate 3.6
jwst_footprints - Travis and setup.py indicate >= 3.6
msaviz - Travis indicates 3.6, setup.py indicates 3.5, conda instructions just say python=3
mirage - conda environment allows for 3.6 or 3.7, Travis is testing 3.6
awesimsoss - Travis, conda, setup.py all using 3.6
webbpsf - conda and setupy indicate >= 3.6, Travis is testing 3.7
exoctk - Supports 3.6 and 3.7




## Short description

We require that all Python software 'support' python version 3.6 or higher.  We define 'support' in this context such that:

- The python software is fully operational with no errors when invoked from an interpreter that uses Python 3.6 or higher,
- Any future contributions to the software must also adhere to the above requirement
- Any provided environment file(s) in the repository (i.e. `environment.yml`, `requirements.txt`, `setup.py`), must all list a consistent version of python.


## Importance of this standard



## How to apply this standard

For software that must be upgraded from Python 2.x to Python 3.x, the tool [`2to3`](https://docs.python.org/2/library/2to3.html) can be used to show (and optionally apply) all of the necessary changes.  For a general description of what aspects of the Python 2.x code must be changed in order to comply with Python 3.x, see the [official Python documentation on 'updating your code'](https://docs.python.org/3/howto/pyporting.html#update-your-code).

For software that must be upgraded from Python<=3.5 to Python>=3.6, see

- Point to documentation on differences between python versions (especially 3.6 vs 3.7)


## Useful Links

- [`2to3`](https://docs.python.org/2/library/2to3.html)
- Python 3.6 to 3.7 differences
-
