# Software Must Have Installation and Usage Documentation

This is one of the tier 1 standards. See full list [on the main page](../README.md).

## Short description
It is important to explicitly state how users can install and use the software. Such information must either be explicitly documented in or linked to on a JDox page.

## Importance of this standard
A description of how users can install and use the software will allow them to begin using the software as quickly and easily as possible.  It is also important that this documentation is easy to find by possible users. For this reason, we have set [JDox](https://jwst-docs.stsci.edu/) to be a common location where users can find installation information for all of the INS JWST user-facing software.

## Options for this standard
If you would like the installation and usage documentation to live outside of but be linked in JDox, some possible locations include:
- The `README` file in the outward-facing repository (e.g. GitHub)
- A separate, external documentation website (e.g. Read The Docs)

## How to apply this standard
How to create/add to a JDox page:
- If you need access to edit pages on [the JDox staging website](https://jwst-docs.stsci.edu/display/JDOX) contact to Shireen Gonzaga
- Follow the [JDox Author's Guide](https://outerspace.stsci.edu/display/JWSTDG/JWST+User+Documentation+Author%27s+Guide) and [JDOX Style Guide](https://outerspace.stsci.edu/display/JWSTDG/JWST+User+Documentation+Style+Guide) to create/edit your page
    - If you are editing a page, as a courtesy please talk to the original creator/last modifier of the page
- If you have any questions about this process, contact Shireen Gonzaga, Ori Fox, and/or Stephanie La Massa

What information to include:
- The command to install software via `pip` or `conda`. See [here](conda_or_pip.md) for requirement.
- The command to download/install software directly from repository (if relevant)
- How to download and use the `environment.yml` and/or `requirements.txt` file to set up a software environment. See [here](software_environment.md) for relevant links.
- Any known installation or usage issues

Not required, but useful information to include:
- Link to repository
- Link to documentation for software if it exists outside JDox
