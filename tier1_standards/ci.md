# Software Must Use Continuous Integration

This is one of the tier 1 standards. See full list [on the main page](../README.md).

## Short description
Continuous Integration (CI) is a practice where developers regularly integrate their code changes into the main repository and validate their changes by running automated builds and tests. This integration should occur before code changes are merged into production to ensure that the new changes do not break the existing software.

## Importance of this standard
CI's automated building and testing allows developers to:
- Reduce their manual testing effort
- Avoid long integration processes for large code changes
- Test changes before merging to avoid breaking the code base
- Find bugs early in the development
- Easily test the installation of their package

## Options for this standard
For a summary of the different CI options available at STScI, see the STScI Style Guide on CI [here](https://github.com/spacetelescope/style-guides/blob/master/guides/python-testing.md/#continuous-integration)

## How to apply this standard
The existence of unit tests is highly encouraged as part of this standard, but not required. Since CI also tests package installation, it can be set up without the existence of any unit tests.

See a guide on how to set up multiple CI options from the [STScI Training Library](https://innerspace.stsci.edu/display/INSTL/Continuous+Integration+and+Testing)

## Useful Links

- [GitHub Actions Quickstart Tutorial](https://docs.github.com/en/actions/quickstart)
- [GitHub Actions Python Tutorial](https://docs.github.com/en/actions/guides/building-and-testing-python)
- [General information on CI by Thought Works](https://www.thoughtworks.com/continuous-integration)
- [General information on CI by Atlassian](https://www.atlassian.com/continuous-delivery/principles/continuous-integration-vs-delivery-vs-deployment)
