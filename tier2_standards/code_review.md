# Project Must Utilize Code Review/Approval for New Changes

This is one of the tier 2 standards. See full list [on the main page](../README.md).

## Short description

Code review is the practice of one or more developers checking another developer's work to find any issues and/or improve the code.

## Importance of this standard

Developers looking at one another's code helps to limit the number of bugs, typos, and formatting mistakes from ending up in the final software. Code review also enables knowledge transfer, as developers are exposed to code that they didn't write, but may need to use in the future.

## Options for this standard

Code reviews can happen with any number of developers and can range from a more removed act of reviewing pull requests to large sit down sessions where an entire team looks at a piece of code. Due to the size and nature of the INS teams, we will focus on implementing the former type of code review.

Whenever a pull request or merge request is submitted, we are requiring that someone should check the code changes before the request is merged. One way to streamline is process is to have the developer assign a specific person to review the request. See below for instructions on how to do this for GitHub and GitLab.
- [Assigning a reviewer on GitHub](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/requesting-a-pull-request-review)
- [Assigning a reviewer on GitLab](https://docs.gitlab.com/ee/user/project/merge_requests/merge_request_approvals.html)

We are requiring that an approving review is submitted before any pull/merge request is merged into the code base. However, developers who are administrators on the repository can use their discretion to override this in urgent situations. This can be done in GitHub or GitLab by following instructions here:
- [Require code review for PRs in GitHub](https://help.github.com/en/enterprise/2.13/user/articles/enabling-required-reviews-for-pull-requests)
- [Require code review for MRs in GitLab](https://docs.gitlab.com/ee/user/project/merge_requests/merge_request_approvals.html)

Teams should see the [Backup Maintainers Standard](backup_maintainers.md) if they are concerned about not having the staffing to comply with this requirement.

## How to apply this standard

Reviewers should be assigned only once the code is considered complete by the developer. Once assigned, the reviewer can comment on, request changes of, or approve the pull/merge request. Reviewing is usually a cyclic process, where a reviewer may review, request changes, and re-review the code until they are satisfied with the changes.

Some of the things reviewers can look for in their reviews of pull/merge requests are:
- Checking the code covers all the original requirements
- Checking for any bugs in general use cases and edge cases
- Checking for consistency and legibility of code
- Checking the code matches PEP8 and/or the software's style guide
- Checking there are tests and documentation written for any new code
- Checking that all tests pass in the Continuous Integration build(s)

Something to remember is that all parties should be conscious of staying polite and respectful while participating in a review. Code reviews can quickly become ineffective if the reviewer is disrespectful or the developer is not willing to make changes. Code review should be a time to put egos aside for the sake of good code. See the "Useful Links" section below for a video of a conference talk on how to keep code reviews effective.

## Useful Links

- [STScI's options on git review](https://github.com/spacetelescope/style-guides/blob/master/guides/git-pr-review.md)
- [PyCon 2017 Talk on Effective Code Review](https://www.youtube.com/watch?v=iNG1a--SIlk) (particularly the first half)
