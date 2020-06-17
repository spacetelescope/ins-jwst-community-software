# Project Must Utilize Code Review/Approval for New Changes

This is one of the tier 2 standards. See full list [on the overview page](README.md).

## Short description

Code review is the practice of one of more developers checking another developer's work to find any issues and/or improve the code. 

## Importance of this standard

Developers looking at one another's code helps to limit the number of bugs, typos, and formatting mistakes from ending up in the final software. Code review also enables knowledge transfer, as developers are exposed to code that they didn't write, but may need to use in the future.

## Options for this standard

Code reviews can happen with any number of developers and can range from reviewing pull requests to large sit down sessions where an entire team looks at a piece of code. Due to the size and nature of the INS teams, we will focus on implementing the former type of code review.

While software teams can keep the review process outside of their git workflow, we recommend that they consider implementing required code reviews before any pull/merge requests are merged into the code base. This can be done for GitHub or GitLab by following instructions here:
- [Require code review for PRs in GitHub](https://help.github.com/en/enterprise/2.13/user/articles/enabling-required-reviews-for-pull-requests)
- [Require code review for MRs in GitLab](https://docs.gitlab.com/ee/user/project/merge_requests/merge_request_approvals.html)

Then when a pull request or merge request is submitted, the developer can assign a specific person to review the request. See below for instructions on how to do this for GitHub and GitLab.
- [Assigning a reviewer on GitHub](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/requesting-a-pull-request-review)
- [Assigning a reviewer on GitLab](https://docs.gitlab.com/ee/user/project/merge_requests/merge_request_approvals.html)

The software teams should also decide who is responsible for merging the pull/merge request, the submitter or the reviewer. This is a decision we leave up the teams.

## How to apply this standard

Once assigned, the reviewer can comment, request changes, or approve the pull/merge request. 


Some of the things reviewers can look for in their reviews of pull/merge requests are:
- Checking the code covers all the original requirements
- Checking for any bugs in general use cases and edge cases
- Checking for consistency and legibility of code
- Checking the code matches the software's style guide
- Checking there are tests and documentation written for any new code

## Useful Links
- [STScI's options on git review](https://github.com/spacetelescope/style-guides/blob/master/guides/git-pr-review.md)
- [PyCon 2017 Talk on Effective Code Review](https://www.youtube.com/watch?v=iNG1a--SIlk)
