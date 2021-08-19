# Software Must Meet Basic Standards for Protecting It's `main` Branch

This is one of the tier 1 standards. See full list [on the overview page](README.md).

## Short description
Protecting the `main` branch (formally known as the `master` branch) means setting up safeguards within the repository settings to prevent any un-checked changes from being applied to the production level of the code.

## Importance of this standard
The main branch of a repository is the official 'production' version of the code and for this reason, developers must be very careful when merging changes into it. A major way to avoid the potential disaster of an unintended push to `main` is to protect the `main` branch by blocking developers from making un-checked changes via settings within the repository.

Examples of possibly huge problems that can be prevented with a protected `main` branch includes accidentally force pushing a bad change to `main` or even accidentally deleting the `main` branch. While we trust our developers, mistakes can happen, and it never hurts to be careful.

## Options for this standard
For all INS software, we define "protecting" the `main` branch to include the following:
- Disabling force pushing to `main` and requiring pull/merge requests before merging any code into `main`
- Restricting developers from deleting `main`
- Requiring continuous integration checks to pass before merging is allowed

Depending on the repository hosting service you use, you may also be able to set extra protections for `main` (or other branches). These can include things like requiring pull/merge requests to be approved by one or more people, or requiring commits to be signed. These protections are up to the development team to decide if they are applicable.

The development team may also choose who these protections apply to. The most common approaches are to have it apply to everyone involved in with the software or have administrators of the repository be exempt from some/all of these rules.

## How to apply this standard
- Instructions for how to [set up a protected main branch on GitHub](https://help.github.com/en/articles/configuring-protected-branches)
- Instructions for how to [set up a protected main branch on GitLab](https://docs.gitlab.com/ee/user/project/protected_branches.html)
