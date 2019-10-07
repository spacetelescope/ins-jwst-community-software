# Software Must Have a Recorded Environment

This is one of the tier 1 software standards. See full list [here](tier1_standards_overview.md)

## Short description
Environment files are a way to share conda environments in a format that allows users to create an environment from the file using a one-line command.

## Importance of standard
Including environment files in your repository leads for an easier installation process for your users as it allows them to create a conda environment that is almost guaranteed to be able to successfully run the software.

## How to apply this standard
Once created, your environment file should live in the top level of your repository

To create an environment file by creating a new environment and saving it:
- Create your basic environment with `conda create -n env_name python=X.X`
- Install all required packages. For this you have options:
    - You can use your setup.py file's requirements by just running `python setup.py install`
    - You can install requirements by hand, making sure to check the package versions
- Confirm your tool runs
- Export your environment to a file with `conda env export > environment.yml`

To create an environment file by hand:
- Create your YAML file with the command `touch environment.yml`
- In your favorite text editor, fill out the file. See some of [conda's examples](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#creating-an-environment-file-manually)

## Useful Links
Conda Documentation on Environments: https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#