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




## Importance of this standard


## Options for this standard


## How to apply this standard

- Point to documentation on differences between python versions (especially 3.6 vs 3.7)


## Useful Links
