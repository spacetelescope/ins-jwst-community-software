# Software Must Have a Recorded Environment

This is one of the tier 1 software standards. See full list [here](tier1_standards_overview.md)

## Short description
Files that contain information on the environment set-up needed to run your tool, like `environment.yml` and `requirements.txt` files, are a good way to share environment information in a format that allows users to create or update an environment from the file using a one-line command.

## Importance of standard
Including files with required package information in your repository leads for an easier installation process for your users as it allows them to create or update a conda environment that is almost guaranteed to be able to successfully run the software.

## Options for this standard
The two common options for this standard are `environment.yml` and `requirements.txt` files.

## How to apply this standard
Instructions to create an `environment.yml` file:
- [From an existing environment](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#sharing-an-environment)
- [By hand](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#creating-an-environment-file-manually)

Instructions to create a `requirements.txt` file:
- [From an existing environment](https://pip.readthedocs.io/en/1.1/requirements.html#freezing-requirements)
- [By hand](https://pip.readthedocs.io/en/1.1/requirements.html#the-requirements-file-format)

Once created, this file should live in the top level of your repository.

## Useful Links
- [Conda's documentation on environments](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html)
- [Pip's documentation on requirements files](https://pip.readthedocs.io/en/1.1/requirements.html)