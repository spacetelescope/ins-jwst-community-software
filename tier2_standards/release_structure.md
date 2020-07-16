# Project Must Define a Consistent Release Procedure

This is one of the tier 2 standards. See full list [on the overview page](README.md).

- We will build two examples (one for PyPi-based project, one for conda-based project)

## Short description

We require that teams adopt a consistent procedure for making a new 'release' and document said procedure somewhere within the repository and/or project documentation.  In this context, we define a 'release' as the tagging of a new software version and uploading that version of the software to either PyPI or Conda (as was part in the [Tier 1 standards](https://github.com/spacetelescope/ins-jwst-community-software/blob/master/tier1_standards/conda_or_pip.md)).


## Importance of this standard

Adopting a consistent release procedure has several benefits.

- Something about anyone on team being able perform a release
- Consistent expectations from users on the scale of a release
- Meaningful releases.


## Options for this standard

Below we provide two examples of release structures, one that uses PyPI, and one that uses Conda.  We encourage teams to tweak these examples as necessary based on the specifics of your project.  Teams may also opt to create their own release structure document from scratch.

Example using **PyPI**:

```
The <project> team performs a software release at <some occaison>. We employ the following procedure for creating a new release:

    1. Create a new branch for changes related to the version release procedure
    2. Update appropriate version numbers in <locations that store the version number>,
    3. Update the release notes
    4. Open, review, and merge pull request with the release procedure changes
    5. Create a new tag/release on GitHub/GitLab
    6. Upload new version of software to PyPI

Detailed instructions for performing a release are given below:

1. Create a new branch for changes related to the version release procedure

Make sure that your local version of the <develop branch> is up-to-date. A new branch with the naming convention vx.y.z should be opened off of the <develop branch>, where x.y.z is the version number of the release (e.g. v0.4.1). This branch should be used for the changes described in the rest of this document.

2. Update the version number in <locations that store the version number>

The VERSION variable in setup.py should be updated to the new version number, using the x.y.z convention.  <Update any other locations of hard-coded version numbers>

3. Update the release notes

In <location of release notes>, write a concise but detailed description of all of the notable changes that have occurred since the last release. One way to acquire this information is to scroll through the commit history of the project, and look for commits in which a pull request was merged.

4. Open, review, and merge pull requests with the release procedure changes

Once you've committed the changes from (2), (3), and (4) in your branch, push your branch to GitHub/GitLab using the upstream remote, open two pull requests: one that points to the production branch (e.g. `master`), and one that points to <develop branch>. Assign reviewers. Either you or the reviewer should eventually merge these pull requests.

5. Create a new tag/release on GitHub/GitLab

Once the pull request into the production branch from (5) has been merged, click on the releases button on the main page of the repository, then hit the "Draft a new release button". The "Tag version" should be the version number of the release, the "Target" should be the production branch, the "Release title" should (also) be the version number of the release, and the "Description" should match that of the changelog entry in (4). Once all of that information is added, hit the big green "Publish" release button.

6. Upload new version of software to PyPI

To upload the new tagged version of the software to PyPI, run the following:

- ``python setup.py sdist bdist_wheel``
- ``twine upload -u '$<pypi_username>' -p '$<pypi_password>' --repository-url https://upload.pypi.org/legacy/ --skip-existing dist/*``
```

Example using **astroconda**:

```
The <project> team performs a software release at <some occaison>. We employ the following procedure for creating a new release:

    1. Create a new branch for changes related to the version release procedure
    2. Update appropriate version numbers in <locations that store the version number>,
    3. Update the release notes
    4. Open, review, and merge pull request with the release procedure changes
    5. Create a new tag/release on GitHub/GitLab
    6. Upload new version of software to ``astroconda``

Detailed instructions for performing a release are given below:

1. Create a new branch for changes related to the version release procedure

Make sure that your local version of the <develop branch> is up-to-date. A new branch with the naming convention vx.y.z should be opened off of the <develop branch>, where x.y.z is the version number of the release (e.g. v0.4.1). This branch should be used for the changes described in the rest of this document.

2. Update the version number in <locations that store the version number>

The VERSION variable in setup.py should be updated to the new version number, using the x.y.z convention.  <Update any other locations of hard-coded version numbers>

3. Update the release notes

In <location of release notes>, write a concise but detailed description of all of the notable changes that have occurred since the last release. One way to acquire this information is to scroll through the commit history of the project, and look for commits in which a pull request was merged.

4. Open, review, and merge pull requests with the release procedure changes

Once you've committed the changes from (2), (3), and (4) in your branch, push your branch to GitHub/GitLab using the upstream remote, open two pull requests: one that points to the production branch (e.g. `master`), and one that points to <develop branch>. Assign reviewers. Either you or the reviewer should eventually merge these pull requests.

5. Create a new tag/release on GitHub/GitLab

Once the pull request into the production branch from (5) has been merged, click on the releases button on the main page of the repository, then hit the "Draft a new release button". The "Tag version" should be the version number of the release, the "Target" should be the production branch, the "Release title" should (also) be the version number of the release, and the "Description" should match that of the changelog entry in (4). Once all of that information is added, hit the big green "Publish" release button.

6. Upload new version of software to ``astroconda``

To upload the new tagged version of the software to ``astroconda``, run the following:

- ``cd astroconda-contrib``
- ``git checkout -tb update-<my_package> master``
- Open <my_package>/meta.yaml in text editor
- Modify {% set version = '<version>' %}, close, and save
- ``conda build -c http://ssb.stsci.edu/astroconda --skip-existing --python=<python_version> <my_package>``
- ``git add <my_package>/meta.yaml``
- ``git commit -m 'Updated <my_package> <old_version> -> <new_version>'``
- ``git push origin update-<my_package>``
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

- [Instructions for uploading a package to `conda` or `pip`](https://github.com/spacetelescope/ins-jwst-community-software/blob/master/tier1_standards/conda_or_pip.md#how-to-apply-this-standard)
- [STScI Style Guide for Release Workflow](https://github.com/spacetelescope/style-guides/blob/master/guides/release-workflow.md)
