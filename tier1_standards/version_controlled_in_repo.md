# Software Must Be Version Controlled in a Software Repository

This is one of the tier 1 software standards. See full list [here](tier1_standards_overview.md)

## Short description
A version controlled repository is a set of directories and files that have their changes tracked such that old versions of the repository can be viewed later.

## Importance of standard
Hosting your software in a version controlled repository has a number of benefits. First and foremost, since it keeps a history of changes it makes it possible to trace any problems in code to specific changes or revert your software if a mistake is made.

Version controlled repositories also allow for more streamlined development as multiple people can work on the code base at once but in different streams which a version control system can help merge back together and handle any conflicting changes. There are many possible work flows that can be used when editing version controlled data, a basic overview of which can be read about [here](https://www.atlassian.com/git/tutorials/comparing-workflows).

## Options for this standard
There are a few different options hosting for version controlled repository. STScI mainly using GitHub or GitLab, so we would recommend using one of these. However there are many other options including Mercurial, Perforce, and Apache Subversion.

## How to apply this standard
Focusing on GitHub and GitLab, here is some information on uploading/transferring projects:
- To upload an existing project to GitHub:
    - [From a local version of the repository](https://help.github.com/en/articles/adding-an-existing-project-to-github-using-the-command-line)
    - [From another version control system](https://help.github.com/en/articles/importing-source-code-to-github)
- To upload an existing project to GitLab:
    - [From a local version of the repository](https://docs.gitlab.com/ee/gitlab-basics/create-project.html#push-to-create-a-new-project)
    - [From another version control system](https://docs.gitlab.com/ee/user/project/import/index.html)

When setting up your repository, there are some conventions that should be met - see the [STScI Style Guide's list of repository conventions](https://github.com/spacetelescope/style-guides/blob/master/guides/github-repositories.md#conventions) for these. While all these should be met at some point, if you are creating a brand new repository we suggest that you focus on: 
- [Name of repository](https://github.com/spacetelescope/style-guides/blob/master/guides/github-repositories.md#naming)
- [Description of repository](https://github.com/spacetelescope/style-guides/blob/master/guides/github-repositories.md#repository-descriptions)
- [Including a README.md file](https://github.com/spacetelescope/style-guides/blob/master/guides/github-repositories.md#readmemd)
- [Including a LICENSE file](https://github.com/spacetelescope/style-guides/blob/master/guides/github-repositories.md#license) (also see [our standard](license_file.md) which references the STScI style guide)
- [Applying release conventions](https://github.com/spacetelescope/style-guides/blob/master/guides/github-repositories.md#releases) (also see [our standard](versioned_releases.md) which references the STScI style guide)

## Useful Links
- [More information about git](https://git-scm.com/about)
- [An example GitHub repository from the STScI Style Guide](https://github.com/spacetelescope/stsci-package-template)