# Project Must Provide Release Notes

This is one of the tier 2 standards. See full list [on the overview page](README.md).

## Short description

Release notes are a way to document the updates made to a code base that are included in a release. They serve as a documented history of the software and are updated during every release.

## Importance of this standard

Release notes help both the developer and the user of a piece of software.

Developers use release notes to track their own changes and communicate effectively with their users about why updating to the latest version of the code is particularly important. Keeping users on the latest version helps streamline bug reporting to only include real bugs that are still present in the current version of the software.

Users of software can check release notes to learn about new functionality, see if any changes will affect their own code, or see if any problems they've run into were bugs that have now been fixed.

## Options for this standard

There are two main ways release notes can be included in a repository.

- Developers can use a single `.txt` or `.rst` file to contain a running list of releases and the changes included in them. This type of file is usually named something like `release_notes.txt`, `changelog.txt`, or something similar, and lives either in the top level of the repository or in the `docs/` sub-directory.
- If the repository uses GitHub/GitLab's releases section, they can also use the notes section provided when submitting a release. These notes will remain in the "Releases" section of GitHub/GitLab for users to look at.

## How to apply this standard

It is up to the developers to decide what information they want to include in their release notes. Release notes can be kept short or be longer. Some ideas of content that can be included are:
- New features
- Enhancements to current features
- Bug fixes
- Compatibility changes (e.g. requires newer versions of Python or dependency packages)
- Documentation updates
- Infrastructure fixes (e.g. changes to `setup.py` files, CI files, testing improvements, etc)
- Known issues

Developers also have options when formatting their release notes. They can include any of the following:
- Document the version number and release date (these are particularly important)
- Link to specific Issues and/or Pull Requests
- List the author of each of the changes
- Include small lines of code for any new commands

Developers should write release notes with their user community in mind: the writing shouldn't be vague, jargon should be kept to a minimum, acronyms should be explained, etc.

## Useful Links

Check out some examples of release note formatting here:
- [The JWST Pipeline's CHANGES.rst](https://github.com/spacetelescope/jwst/blob/master/CHANGES.rst)
- [Photutil's CHANGES.rst](https://github.com/astropy/photutils/blob/master/CHANGES.rst)
- [ASDF's CHANGELOG.md](https://github.com/asdf-vm/asdf/blob/master/CHANGELOG.md)
- [Pytest's Changelog.rst](https://github.com/pytest-dev/pytest/blob/master/doc/en/changelog.rst)
