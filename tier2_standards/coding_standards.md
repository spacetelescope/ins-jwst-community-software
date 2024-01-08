# Software Must Enforce Coding Standards

This is one of the tier 2 standards. See full list [on the main page](../README.md).

## Short description

Coding standards serve as a style guide or set of best practices for writing code.

## Importance of this standard

Consistent coding standards across a piece of software improves the overall quality of the code. It make code more readable both for current and future developers which in turn helps it to be more maintainable.

## Options for this standard

Python's main style guide is named the Python Enhancement Proposal #8 or "`PEP8`" and it defines a way of formatting Python code that is widely accepted by the community. Software teams are encouraged to follow `PEP8` standards where appropriate.

Teams are allowed to deviate from these standards in certain cases, for example, ignoring a requirement that may be considered "overkill", or choosing to slightly modified standard. However, the final code base should be reasonably self-consistent and readable.

Below are a list of standards that we have identified as 'overkill'.  Teams may choose to ignore them if they see fit:
- `W191 indentation contains tabs`
- `W291 trailing whitespace`
- `W292 no newline at end of file`
- `W293 blank line contains whitespace`
- `W391 blank line at end of file`
- `W505 doc line too long`
- `W605 invalid escape sequence`
- `E101 indentation contains mixed spaces and tabs`
- `E123 closing bracket does not match indentation of opening bracket's line`
- `E124 closing bracket does not match visual indentation`
- `E401 multiple imports on one line`
- `E501 line too long`
- `E502 the backslash is redundant`

## Linting

Linters are programs that analyize codes to check for bugs, and code style violations.

## Why Use A Linter

Using a linter enforces good programming habits that can sometime slip through the cracks. It enables a code base to be uniform across modules independent of the contributor. It can catch the coding standards that fall outside of the 'overkill' scope.

## How to apply this standard

If you require assistance, we can help the teams get started, by providing a report detailing the current state of a repository compared to `PEP8` standards (with the standards we deemed to be "overkill" listed above ignored). These types of reports can be created using Python packages that compare the contents of a file, folder, repository, etc. to `PEP8` standards and return a report of any disagreements.

Software teams should make an attempt to improve their code to be more in line with the `PEP8` standards put forward by Python. Enforcing linting on code merges is the favored method to enforce this standard.  However if for some reason this practice does not work for your project, you can work with us to find a solution.  A reasonable attempt at updating the code to these standards is expected.  

You can use your preferred linter, and can start by looking at the following 2 options:

- [ruff](https://pypi.org/project/ruff/)
- [pycodestyle](https://pypi.org/project/pycodestyle/)

Teams can improve their code using some of the following methods:

- Reading about [`PEP8` requirements](https://www.python.org/dev/peps/pep-0008/) and checking and changing code by hand
- Using a package that checks code style against `PEP8` like [flake8](https://flake8.pycqa.org/en/latest/), [`pylint`](https://www.pylint.org/), [pycodestyle](https://pep8.readthedocs.io/en/latest/intro.html), etc. and changing code by hand
- Using a package that checks and changes code to match style guides like [`autopep8`](https://pep8.readthedocs.io/en/latest/intro.html)

We will not be setting a percentage improvement in `PEP8` adherence, but due to the mission office's strong support of this standard, we will be talking with each team about their justification for their code being improved, readable, and maintainable.
