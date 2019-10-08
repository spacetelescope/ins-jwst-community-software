# ins-software-standards

This repository is a part of an initiative to have all software tools for the JWST user community that are developed/maintained by the Instruments Division (INS) meet accepted software standards. This includes the software being robust, maintainable, documented, and supported. The contents of this repository aims to describe these standards for the INS software tools and encourage a common approach across projects.

This work is managed by the INS Software Development Leads for this project Matthew Bourque [@bourque](https://github.com/bourque) and Shannon Osborne [@shanosborne](https://github.com/shanosborne)

## Contents

The software standards have been split into "tier 1" and "tier 2" goals.

To meet the [Tier 1 Software Standards](tier1_standards/tier1_standards_overview.md) the tool must:
- Be version controlled in a software repository using a version control system (e.g. ``git``)
- Have a method of versioning software (e.g. GitHub tag)
- Use an issue tracking system (e.g. GitHub Issues, Jira Issues)
- Have a valid package structure such that it is installable via ``python setup.py``
- Be downloadable and installable via ``conda`` and/or ``pip``
- Have a recorded software environment (e.g. ``environment.yml``, ``requirements.txt``)
- Use continuous integration (e.g. ``Travis``, ``Jenkins``)
- Use a workflow that protects a ``master`` or production branch
- Have documentation that describes how to install and use the tool in JDox
- Have a ``LICENSE`` file
- Meet basic security standards

To meet the [Tier 2 Software Standards](tier2_standards/tier2_standards_overview.md) the tool must:
- Have a ``Code of Conduct``
- Use continuous deployment
- Have documented reasoning of when/why to release a new version
- Utilize code review (when appropriate)
- Have a documented ``git`` workflow
- Have backups for its maintainers/developers
- Enforce language-specific coding standards
- Have an automated dependency controller


## Contributing

If you want to suggest changes to this content do the following:
1. Create a fork of this repository
2. Make a local clone of your fork
3. Ensure your personal fork is pointing upstream properly
4. Create a branch on that personal fork
5. Make your changes
6. Push that branch to your personal GitHub repository (i.e. ``origin``)
7. On the ``spacetelescope`` repository, create a pull request
8. Assign a reviewer (either ``@bourque`` or ``@shanosborne``)
9. Iterate with the reviewer over any needed changes until the reviewer accepts and merges your branch
10. Delete your local copy of your branch

## Questions?

Any questions about this effort may be directed to bourque@stsci.edu and sosborne@stsci.edu
