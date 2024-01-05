# Project Must Enforce Code Style/Linting

This is one of the tier 2 standards. See full list [on the main page](../README.md).

## Short description

Linters are programs that analyize codes to check for bugs, and code style violations.

## Importance of this standard

Using a linter enforces good programming habits that can sometime slip through the cracks. It enables a code base to be uniform across modules independent of the contributor.

## Options for this standard

- [pycodestyle](https://pypi.org/project/pycodestyle/)
- [ruff](https://pypi.org/project/ruff/)

## How to apply this standard

Software teams should consider what linting rules to follow based on what the scope of their project. A [list of error codes](https://pep8.readthedocs.io/en/release-1.7.x/intro.html#error-codes) can be found here in the [PEP 8](https://peps.python.org/pep-0008/) documentation. Some software teams will choose to ignore certain errors based on the needs of the project. Error codes can be passed via the command line as an arguement using the `--ignore`