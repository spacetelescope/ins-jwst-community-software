# Project Have Some Unit, Integration, and/or End-to-End Tests

This is one of the tier 2 standards. See full list [on the overview page](README.md).

## Short description

Software tests are pieces of code, often functions or classes, that are written to check that different parts of a code base are working as expected.

## Importance of this standard

When writing new pieces of code, developers will usually run a few checks to make sure the change worked as they expected. However, it's almost impossible to fully check with every change that nothing else was accidentally affected in the process.

For this reason, automated tests are an important part of writing software. These pre-written tests can be easily run with every new change to the software and can be used to confirm that these new changes work as expected without breaking anything else in the code base.

Alongside self-checking your code and participating in code review, running automated tests is a great way to prevent accidental bugs from making it into your code. This is especially important as developers move between projects and the current maintainer of the code base isn't the person who originally wrote it.

## Options for this standard

While there are many different types of testing software, we will focus on unit, integration, and end-to-end tests:
- Unit tests check that the code works. For example, testing a single function or class runs as expected. See the STScI Style Guide's description of unit tests [here.](https://github.com/spacetelescope/style-guides/blob/master/guides/python-testing.md/#types-of-tests)
- Integration tests check that different parts of the code base interact correctly with each other. For example, testing that 2 classes in separate modules work together as expected.
- End-to-end tests check that the entire software works and the requirements are met as expected. For example, testing that a common function call that users would make to your software returns the correct results.

While it is important to touch on all aspects of these types of testing, prioritizing is key if you are starting from zero tests. We recommended (with support from the JWST mission office) that *end-to-end tests should be the first priority for software with no automated tests.* On the other hand, software that already has some tests will have to consider which testing types, if any, they are lacking.

Along with including different types of tests, making sure your tests cover all parts of your code is an important step. One way to check how much of your code is used when you run your tests is to generate a coverage report. Coverage reports can be created with certain packages (see more below) which run your tests and log which parts of your code are interacted with by your tests. The final report will often contain the overall percentage of code lines that are run during your tests, the percentage of lines for each individual file, and exactly which lines are missed. This is a great resource to help prompt you when looking for which parts of the code still need to be tested.

One important note: Software with good coverage is not the same as software that is well tested. It is only an indicator of how widespread your testing is, not how accurate it is. Be wary of aiming for 100% coverage at the expense of writing good tests.

We are not requiring software to have 100% testing coverage - it is not only unreasonable but also often un-necessary to reach that coverage level. Instead, we will be asking teams to show that they have some test coverage and that it is to a level that they deem appropriate for their software.

We have summarized our requirements and recommendations for this tier 2 standard below:
- We are requiring the following:
  - We require at least some automated tests exist for the code base and live in the software repository
  - We require that these tests cover the main functionality of the software at a minimum
  - We require all tests that can be run in Continuous Integration (CI) builds to be run there (e.g. some user interface tests can't be run on CI)
  - We will require a meeting where teams can describe/demonstrate their testing structure and explain why the level of testing is acceptable for their software
- We are recommending the following:
  - We strongly recommend common automated testing tools. The STScI Style Guide recommends `pytest` so we will recommend this as well, but teams do have other options like `unittest` or `nosetest`. In order to facilitate moving between projects in INS, strong justification will be needed to use a testing framework other than `pytest` for new projects.
  - We recommend teams include a mixture of unit, integration, and end-to-end tests as applicable for their software

## How to apply this standard

How to write tests:
- Keep in mind that the goal when writing tests is to have code that you would want to run that would confirm that your software is still working after you made a large change.
- Check out the extensive `pytest` documentation online. See their [main documentation page](https://docs.pytest.org/en/stable/index.html) for an introduction to writing tests.
- Check out the [STScI Style Guide's documentation on Python testing](https://github.com/spacetelescope/style-guides/blob/master/guides/python-testing.md/#testing-python-packages) for information on things like framework options, testing layout, and ideas for what to test.
- Use a self-consistent format when writing tests. Tests are usually formatted as functions or classes and usually live in files named `test_<what-is-tested>.py` in their own sub-directory named `tests` inside your repository (e.g. `repo-name/repo-name/tests/test_conversions.py`)

How to run tests automatically as part of your CI builds:
- You can set up your repository to automatically run all your tests every time you push a new commit to an open pull/merge request. In general, this is done by adding a command after your installation command that runs your tests (e.g. the command: `pytest`) to your CI file (either `travis.yml` or `Jenkinsfile`).
- To add a testing command to Travis CI, check out [Travis's testing documentation](https://blog.travis-ci.com/2019-08-07-extensive-python-testing-on-travis-ci)
- To add a testing command to Jenkins CI, as per the STScI Style Guide's suggestion see the [Innerspace page on Jenkins](https://innerspace.stsci.edu/pages/viewpage.action?spaceKey=SSR&title=Users+Guide%3A+Running+Regression+Tests). In particular, scroll down to the section titled "Running Tests Using Jenkins".

How to check test coverage (optional):
- Developers can create coverage reports locally using [`pytest-cov`](https://pytest-cov.readthedocs.io/en/latest/readme.html) and/or [`coverage.py`](https://coverage.readthedocs.io/en/latest/)
- Developers can create coverage reports automatically as part of their continuous integration setup in their repository using a package like `CodeCov` or `Coveralls`. See the STScI Style Guide's recommendation [here](https://github.com/spacetelescope/style-guides/blob/master/guides/python-testing.md/#automated-test-code-coverage)

## Useful Links

- [A comprehensive list of `pytest` examples](https://docs.pytest.org/en/stable/example/index.html)
- [STScI's main python testing page](https://github.com/spacetelescope/style-guides/blob/master/guides/python-testing.md)
- [Unittest documentation](https://docs.python.org/3/library/unittest.html)
- [Nosetest documentation](https://nose.readthedocs.io/en/latest/)
