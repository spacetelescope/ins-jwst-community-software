# Software Must Have Documentation On It's Installation

This is one of the tier 1 software standards. See full list [here](tier1_standards_overview.md)

## Short description
Included in the general documentation for how to use a piece of software, it is important to also explicitly state how users can install the tool. Information on how to install your software must either be explicitly documented in or linked to on a JDox page.

## Importance of standard
A description of how users can install your tool will help streamline their installation process and let them move on to using your software as quickly as possible.
 
It is also important that this installation documentation be easy to find by possible users. For this reason, we have set [JDox](https://jwst-docs.stsci.edu/) to be a common location where users can find installation information for all of the INS software.

## Options for this standard
If you would like your installation documentation to live outside of but be linked in JDox, some possible locations include:
- Your README file in your outward-facing repository (e.g. GitHub)
- Your own documentation website (e.g. Read The Docs)

## How to apply this standard
How to create/add to a JDox page:
- If you need access to edit pages on [the JDox staging website](https://jwst-docs.stsci.edu/display/JDOX) speak to Shireen Gonzaga
- Follow the [JDox Author's Guide](https://outerspace.stsci.edu/display/JWSTDG/JWST+User+Documentation+Author%27s+Guide) and [JDOX Style Guide](https://outerspace.stsci.edu/display/JWSTDG/JWST+User+Documentation+Style+Guide) to create/edit your page
    - If you are editing a page, as a courtesy please talk to the original creator/last modifier of the page
- If you have any questions about this process, contact Shireen Gonzaga, Ori Fox, and/or Stephanie La Massa

What information to include:
- Command to install software via pip or conda. See [here](conda_or_pip.md) for requirement.
- Command to install software directly from repository (if relevant)
- The minimum Python version required
- How to download and use the environment.yml file to create an environment. See [conda's information on environment.yml files](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#creating-an-environment-from-an-environment-yml-file) as a starting point
- Any known installation issues

Not required but useful information to include:
- Link to repository
- Link to documentation for software if it exists outside JDox

*IMPORTANT NOTE*: While JDox will be frozen for before the Cycle 1 call, there has been a request to have updates occur before the JWST master class in mid-November. If possible, please make these updates for the master class.
