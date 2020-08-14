# Project Must Have or Reference a Documented ``git`` Workflow

This is one of the tier 2 standards. See full list [on the overview page](README.md).

## Short description

A `git` workflow is a documented set of commands that guide contributors through the various steps needed to work on the software, including things like opening and merging a pull request with proposed software changes and keeping personal forks and/or branches up-to-date with the main repository.  We require that teams provide (or reference) the process that they use to make software changes to their repository.

## Importance of this standard

While `git` is an extremely powerful and important tool for tracking and contributing changes to a software repository, it is also a rather complex tool, and often times there are several ways to achieve the same end result.  A `git` workflow provides contributors of your repository a clear and consistent way to propose and/or make software changes.  Furthermore, having this workflow encapsulated in a document allows contributors to refer back to the workflow at any time.

## Options for this standard

While we do not require teams to use any specific workflow, we highly recommend using either the 'branching' workflow or the 'forking' workflow described in the [STScI Style Guides](https://github.com/spacetelescope/style-guides/blob/master/guides/git-workflow.md).  These two workflows are clear standards amongst the software community, are widely used at STScI, and are well described in various online documentation.  However, team may opt to use a custom workflow for their project if it works well for them.

## How to apply this standard

We require that the chosen `git` workflow is fully documented somewhere within the purview of the repository (e.g. the repository's `README`, a GitHub wiki page, a `CONTRIBUTING.md` file, etc.).  If teams opt to use a workflow that is already documented elsewhere (e.g. the 'branching' or 'forking' workflow in STScI Style Guides), they may simply add a small statement somewhere within their project documentation that indicates which workflow is being used, with appropriate links to the existing documentation.  If teams opt to use a custom workflow, we require that the project documentation contain a full description of the workflow, with step-by-step instructions on how to apply it (similar to the Style Guides workflows).

If teams find that the 'branching' or 'forking' workflow in the STScI Style Guides are close to what they want to use, but not exactly what they want to use, they are welcome to propose changes to the Style Guides document by either contacting Matthew and Shannon with their ideas, or submitting a pull request in the Style Guides repository.

## Useful Links

- [STScI Style Guides `git` workflow page](https://github.com/spacetelescope/style-guides/blob/master/guides/git-workflow.md)
- [Atlassian `git` workflow comparison](https://www.atlassian.com/git/tutorials/comparing-workflows)
