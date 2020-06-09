# Software Must Enforce Coding Standards

This is one of the tier 2 standards. See full list [on the overview page](README.md).

## Short description

Coding standards serve as a style guide or set of best practices for writing code.

## Importance of this standard

Consistent coding standards across a piece of software  improves the overall quality of the code. It make code more readable for current and future developers which in turn helps it be more maintainable.

## Options for this standard

Python's main style guide is named "PEP8" and it defines a way of formatting Python code that is widely accepted by the community. Software teams are encouraged to follow PEP8 standards where appropriate.

Teams are allowed to deviate from these standards in certain cases, for example, ignoring a requirement that may be considered "overkill", or choosing to slightly modified standard. However, the final code base should be reasonably self-consistent and readable.

## How to apply this standard

Software teams should make an attempt to improve their code to be more in line with the PEP8 standards put forward by Python. The extent of this improvement is up the software team, but a reasonable attempt at updating the code to these standards is expected.

To help the teams get started, each team will be given a report detailing the current state of their repository compared to PEP8 standards (with some standards we deem to be "overkill" ignored). These types of reports can be created using Python packages that compare the contents of a file, folder, repository, etc to PEP8 standards and return a report of any disagreements.

Teams can improve their code using some of the following methods: 

- Reading about [PEP8 requirements](https://www.python.org/dev/peps/pep-0008/)
- Using a package that checks code style against PEP8 like [flake8](https://flake8.pycqa.org/en/latest/), [pylint](https://www.pylint.org/), [pycodestyle](https://pep8.readthedocs.io/en/latest/intro.html), etc.
- Using a package that changes code to match style guides like [autopep8](https://pep8.readthedocs.io/en/latest/intro.html)

We will not be setting a percentage improvement in PEP8 adherence, but due to the mission office's strong support of this standard, we will be talking with each team about their justification for their code being improved, readable, and maintainable.
