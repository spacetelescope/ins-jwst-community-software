# INS JWST Community Software

This repository is a part of an initiative to have all software tools for the JWST user community that are developed/maintained by the Instruments Division (INS) meet accepted software standards. This includes the software being robust, maintainable, documented, and supported. The contents of this repository aims to describe these standards for the INS software tools and encourage a common approach across projects.

This work is managed by the INS Software Development Leads for this project Matthew Bourque [@bourque](https://github.com/bourque) and Shannon Osborne [@shanosborne](https://github.com/shanosborne)

## Contents

The software standards have been split into "tier 1" and "tier 2" goals.

Tier 1 standards:
- [Software Must Be Version Controlled in a Software Repository](tier1_standards/version_controlled_in_repo.md)
- [Software Must Be Versioned](tier1_standards/versioned_releases.md)
- [Software Must Use an Issue Tracking System](tier1_standards/issue_tracking_system.md)
- [Software Must Be Installable with `python setup.py install`](tier1_standards/package_structure.md)
- [Software Must Be Available with `conda` or `pip`](tier1_standards/conda_or_pip.md)
- [Software Must Have a Recorded Environment](tier1_standards/software_environment.md)
- [Software Must Use Continuous Integration](tier1_standards/ci.md)
- [Software Must Meet Basic Standards for Protecting It's `master` Branch](tier1_standards/protected_master_branch.md)
- [Software Must Have Installation and Usage Documentation](tier1_standards/documentation.md)
- [Software Must Have a LICENSE File](tier1_standards/license_file.md)
- [Software Must Meet Basic Security Standards](tier1_standards/security_standards.md)

Tier 2 standards:

- [Software Repository Must Have a ``Code of Conduct`` File](tier2_standards/code_of_conduct.md)
- [Project Have Documented Citation Information](tier2_standards/citation_information.md)
- [Software Must Enforce Language-specific Coding Standards (e.g. PEP8)](tier2_standards/coding_standards.md)
- [Software Must Use Python>=3.6 Where Applicable](tier2_standards/python_version.md)
- [Project Must Have or Reference a Documented ``git`` Workflow or Contributor's Guide](tier2_standards/git_workflow.md)
- [Software Must Document Modules, Classes, and/or Functions](tier2_standards/api_documentation.md)
- [Project Have Some Unit and/or Regression Tests](tier2_standards/test_coverage.md)
- [Project Must Define and Document a Consistent Release Proceedure](tier2_standards/release_proceedure.md)
- [Project Must Provide Release Notes](tier2_standards/release_notes.md)
- [Project Must Have Backup Maintainers](tier2_standards/backup_maintainers.md)
- [Project Must Utilize Code Review/Approval for New Changes](tier2_standards/code_review.md)
- [Project Must Use an Automated Dependency Controller](tier2_standards/automated_dependency.md)

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
