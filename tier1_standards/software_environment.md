# Software Must Have a Recorded Environment

This is one of the tier 1 standards. See full list [on the overview page](tier1_standards_overview.md).

## Short description
Files that contain a list of software dependencies that are needed to run the tool, like `environment.yml` and `requirements.txt` files, are a good way to allow users to recreate a software environment in which to run the software.  Environment/requirement files can in turn be made available and version controlled within the software repository, thus capturing a software environment in which the tool will run sucessfully for each version of the code.

## Importance of this standard
Including files with required package information in your repository leads for an easier installation process for users, as it allows them to create or update a conda environment that is likely to be able to successfully run the software.

## Options for this standard
The two common options for this standard are `environment.yml` (to be used with `conda`) and `requirements.txt` (to be used with `pip`) files.

## How to apply this standard
Instructions to create an `environment.yml` file:
- [From an existing environment](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#sharing-an-environment)
- [By hand](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#creating-an-environment-file-manually)

Instructions to create a `requirements.txt` file:
- [From an existing environment](https://pip.readthedocs.io/en/1.1/requirements.html#freezing-requirements)
- [By hand](https://pip.readthedocs.io/en/1.1/requirements.html#the-requirements-file-format)

Once created, this file should live in the top level of the repository.

## Useful Links
- [Conda's documentation on environments](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html)
- [Pip's documentation on requirements files](https://pip.readthedocs.io/en/1.1/requirements.html)