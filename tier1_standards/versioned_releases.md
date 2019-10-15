# Software Must Be Versioned

This is one of the tier 1 software standards. See full list [here](tier1_standards_overview.md)

## Short description
As software is incrementally released, it is common practice to give unique version names or numbers to the newly released code.

## Importance of standard
Attaching version numbers to software releases allow for users, especially less technical users, to easily keep track of changes and determine if an upgrade is needed.

## Options for this standard
As it is ITSD policy is to host your software in a GitHub or GitLab repository, we suggest using GitHub or GitLab tags respectively for versioning your software. 

When naming these versions, we suggest you follow the STScI style guide's recommendation of Semantic Versioning. See the [style guide's description of this system](https://github.com/spacetelescope/style-guides/blob/master/guides/software-versioning.md#software-we-build) for more information. While this is the suggested method, the most important thing is to be consistent and document your versioing method for your users. 

## How to apply this standard
See these how-to articles for creating:
- [GitHub tags](https://help.github.com/en/articles/creating-releases)
- [GitLab tags](https://docs.gitlab.com/ee/university/training/topics/tags.html)

See the [SemVer website](https://semver.org/) and their [FAQ section](https://semver.org/#faq) for details on using their versioning convention.
