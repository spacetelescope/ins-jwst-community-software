# Software Must Be Version Controlled in a Software Repository

This is one of the tier 1 standards. See full list [on the main page](../README.md).

## Short description
A version controlled repository is a set of directories and files that have their changes tracked such that older versions of the software can be retrieved.

## Importance of this standard
Hosting your software in a version controlled repository has a number of benefits. First and foremost, since it keeps a history of changes it makes it possible to trace any problems in code to specific changes or revert your software if a mistake is made.

Version controlled repositories also allow for more streamlined development as multiple people can collaborate on software with a version control system that can help merge together changes and handle conflicting changes. There are many possible workflows that can be used when employig a version control system; a basic overview can be found [here](https://www.atlassian.com/git/tutorials/comparing-workflows).

## Options for this standard
It is [ITSD policy](https://innerspace.stsci.edu/display/EPol/Source+Code+Control) to use `git` as your version control system. Specifically, the policy states that "all STScI products maintain an up-to-date repository on the STScI GitLab solution located on `grit.stsci.edu`, or on `gitar.stsci.edu` for ITAR/EAR-controlled code" and "where necessary to support external collaboration, STScI product teams may use GitHub ... as the primary source control repository, but must also maintain a mirror repository internally on the STScI GitLab."

## How to apply this standard
Here is information on uploading/transferring projects:
- To upload an existing project to GitHub:
    - [From a local version of the repository](https://help.github.com/en/articles/adding-an-existing-project-to-github-using-the-command-line)
    - [From another version control system](https://help.github.com/en/articles/importing-source-code-to-github)
- To upload an existing project to GitLab:
    - [From a local version of the repository](https://docs.gitlab.com/ee/gitlab-basics/create-project.html#push-to-create-a-new-project)
    - [From another version control system](https://docs.gitlab.com/ee/user/project/import/index.html)
- To set up a mirror between GitHub and GitLab, see [GitLab's documentation on pull mirrors](https://docs.gitlab.com/ee/user/project/repository/mirror/pull.html), or see instructions provided below.
    - If you run into password errors, you may need to set up a [GitHub personal access token](https://help.github.com/en/articles/creating-a-personal-access-token-for-the-command-line) (be sure to check the "repo" section), and use that instead of the password when creating the mirror.

When setting up your repository, there are some conventions that should be met - see the [STScI Style Guide's list of repository conventions](https://github.com/spacetelescope/style-guides/blob/master/guides/github-repositories.md#conventions) for these. While all these should be met at some point, if you are creating a brand new repository we suggest that you focus on:
- [Name of repository](https://github.com/spacetelescope/style-guides/blob/master/guides/github-repositories.md#naming)
- [Description of repository](https://github.com/spacetelescope/style-guides/blob/master/guides/github-repositories.md#repository-descriptions)
- [Including a README.md file](https://github.com/spacetelescope/style-guides/blob/master/guides/github-repositories.md#readmemd)
- [Including a LICENSE file](https://github.com/spacetelescope/style-guides/blob/master/guides/github-repositories.md#license) (also see [our standard](license_file.md) which references the STScI style guide)
- [Applying release conventions](https://github.com/spacetelescope/style-guides/blob/master/guides/github-repositories.md#releases) (also see [our standard](versioned_releases.md) which references the STScI style guide)

### Setting up a mirror on GitLab

1. Log into the STScI GitLab instance (https://grit.stsci.edu)
2. Create a new Personal Access Token
    1. Click your personal profile logo (top right of screen) and go to `Settings`
    2. On the left side, click `Access Tokens`
    3. Provide a name for the access token in the `Name` field.  The `Expires at` field can remain blank.
    4. Check all of the boxes under `Scopes`
    5. Click `Create personal access token`
    6. Copy the resulting access token to the clipboard
3. If necessary, create a new GitLab repository for your project
    1. Click the `+` button at the top of the page and select `New Project`
    2. Set up your project accordingly, providing a `Project name`, `Project description`, and `Visibility Level`
    3. Click `Create project`
4. Set up a mirror to the corresponding GitHub repository
    1. On the left side of the page, click `Settings`, then select `Repository`
    2. Click `Expand` under `Mirroring repositories`
    3. Enter the URL for the GitHub repository under `Git repository URL` (e.g. `https://GITHUB_USERNAME@github.com/spacetelescope/REPONAME.git`)
    4. Select `Pull` for `Mirror direction`
    5. Select `Password` for `Authentication method`
    6. Paste Personal Access Token from above in the `Password` field
    7. Click `Mirror` repository

## Useful Links
- [More information about git](https://git-scm.com/about)
- [An example GitHub repository from the STScI Style Guide](https://github.com/spacetelescope/stsci-package-template)
