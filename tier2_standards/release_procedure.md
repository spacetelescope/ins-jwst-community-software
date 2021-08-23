# Project Must Document a Release Procedure

This is one of the tier 2 standards. See full list [on the overview page](README.md).

## Short description

We require that teams adopt a consistent procedure for making a new 'release' and document (or reference an existing document of) said procedure somewhere within the repository and/or project documentation.  In this context, we define a 'release' as the tagging of a new software version and uploading that version of the software to either PyPI or Conda (as was part in the [Tier 1 standards](https://github.com/spacetelescope/ins-jwst-community-software/blob/main/tier1_standards/conda_or_pip.md)).

## Importance of this standard

Adopting a consistent, documented release procedure has several benefits:

- It helps to reduce the learning curve for performing releases, and thus helps to enable any current or future team member to perform a release.
- It makes it clear to contributors which distribution source (i.e. `pypi` or `conda`) is used for releases.
- It serves as an explicit reminder to update/maintain release notes and tagged versions of the software. (For more information, see the [Release Notes Tier 2 standard](release_notes.md) and the [Versioned Releases Tier 1 standard](https://github.com/spacetelescope/ins-jwst-community-software/blob/main/tier1_standards/versioned_releases.md)).

## Options for this standard

Teams may opt to create their own custom release procedure, reference an existing release procedure, or tweak as necessary one of the two examples provided below.  One example releases on `pypi` and the other on `astroconda`.

Example using **PyPI**:

```
The <project> team performs a software release at <some occasion>. We employ the following procedure for creating
a new release:

    1. Create a new branch for changes related to the version release procedure
    2. Update appropriate version numbers in <locations that store the version number>,
    3. Update the release notes
    4. Open, review, and merge pull request with the release procedure changes
    5. Create a new tag/release on GitHub/GitLab
    6. Upload new version of software to PyPI

Detailed instructions for performing a release are given below:

1. Create a new branch for changes related to the version release procedure

Make sure that your local version of the <develop branch> is up-to-date. A new branch with the naming convention
vx.y.z should be opened off of the <develop branch>, where vx.y.z is the version number of the release
(e.g. v0.4.1). This branch should be used for the changes described in the rest of this document.

2. Update the version number in <locations that store the version number>

<Update all locations of hard-coded version numbers. For example, the VERSION variable in setup.py should be
updated to the new version number, using the x.y.z convention.>

3. Update the release notes

In <location of release notes>, write a concise but detailed description of all of the notable changes that have
occurred since the last release. One way to acquire this information is to scroll through the commit history of
the project, and look for commits in which a pull request was merged.

4. Open, review, and merge pull requests with the release procedure changes

Once you've committed the changes from (2), (3), and (4) in your branch, push your branch to GitHub/GitLab using
the upstream remote, open two pull requests: one that points to the production branch (e.g. main), and one
that points to <develop branch>. Assign reviewers. Either you or the reviewer should eventually merge these pull
requests.

5. Create a new tag/release on GitHub/GitLab

Once the pull request into the production branch from (5) has been merged, click on the releases button on the
main page of the repository, then hit the "Draft a new release button". The "Tag version" should be the version
number of the release, the "Target" should be the production branch, the "Release title" should (also) be the
version number of the release, and the "Description" should match that of the changelog entry in (4). Once all
of that information is added, hit the big green "Publish" release button.

6. Upload new version of software to PyPI

To upload the new tagged version of the software to PyPI, run the following:

- python setup.py sdist bdist_wheel
- twine upload -u '$<pypi_username>' -p '$<pypi_password>' --repository-url https://upload.pypi.org/legacy/
  --skip-existing dist/*
```

Example using **astroconda**:

```
The <project> team performs a software release at <some occasion>. We employ the following procedure for creating
a new release:

    1. Create a new branch for changes related to the version release procedure
    2. Update appropriate version numbers in <locations that store the version number>,
    3. Update the release notes
    4. Open, review, and merge pull request with the release procedure changes
    5. Create a new tag/release on GitHub/GitLab
    6. Upload new version of software to astroconda

Detailed instructions for performing a release are given below:

1. Create a new branch for changes related to the version release procedure

Make sure that your local version of the <develop branch> is up-to-date. A new branch with the naming convention
vx.y.z should be opened off of the <develop branch>, where vx.y.z is the version number of the release
(e.g. v0.4.1). This branch should be used for the changes described in the rest of this document.

2. Update the version number in <locations that store the version number>

<Update all locations of hard-coded version numbers. For example, the VERSION variable in setup.py should be
updated to the new version number, using the x.y.z convention.>

3. Update the release notes

In <location of release notes>, write a concise but detailed description of all of the notable changes that have
occurred since the last release. One way to acquire this information is to scroll through the commit history of
the project, and look for commits in which a pull request was merged.

4. Open, review, and merge pull requests with the release procedure changes

Once you've committed the changes from (2), (3), and (4) in your branch, push your branch to GitHub/GitLab using
the upstream remote, open two pull requests: one that points to the production branch (e.g. main), and one
that points to <develop branch>. Assign reviewers. Either you or the reviewer should eventually merge these pull
requests.

5. Create a new tag/release on GitHub/GitLab

Once the pull request into the production branch from (5) has been merged, click on the releases button on the
main page of the repository, then hit the "Draft a new release button". The "Tag version" should be the version
number of the release, the "Target" should be the production branch, the "Release title" should (also) be the
version number of the release, and the "Description" should match that of the changelog entry in (4). Once all
of that information is added, hit the big green "Publish" release button.

6. Upload new version of software to astroconda

To upload the new tagged version of the software to astroconda, run the following:

- cd astroconda-contrib
- git checkout -tb update-<my_package> main
- Open <my_package>/meta.yaml in text editor
- Modify {% set version = '<version>' %}, close, and save
- Run conda build -c http://ssb.stsci.edu/astroconda --skip-existing --python=<python_version> <my_package>
  and verify it passes without error
- git add <my_package>/meta.yaml
- git commit -m 'Updated <my_package> <old_version> -> <new_version>'
- git push origin update-<my_package>
- In a broswer, navigate to  https://github.com/<your_accnount>/astroconda-contrib/tree/update-<my_package>
- Click the “New pull request” button
- Fill out the pull request form
- Click the green “Create pull request” button
```

## How to apply this standard

We require that teams document the release structure somewhere within the repository and/or project documentation.  This could include:

- A new markdown file in the main repository directory (e.g. `RELEASES.md`).
- A dedicated section in the repository `README`.
- A dedicated section in the project wiki on GitHub/GitLab.

Feel free to reach out to Shannon and/or Matthew if some guidance is needed in tweaking the above examples or constructing a new release structure.

## Useful Links

- [Instructions for creating release notes](https://github.com/spacetelescope/ins-jwst-community-software/blob/main/tier2_standards/release_notes.md)
- [Instructions for uploading a package to `conda` or `pip`](https://github.com/spacetelescope/ins-jwst-community-software/blob/main/tier1_standards/conda_or_pip.md#how-to-apply-this-standard)
- [STScI Style Guide for Release Workflow](https://github.com/spacetelescope/style-guides/blob/master/guides/release-workflow.md)
