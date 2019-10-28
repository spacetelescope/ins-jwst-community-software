# Software Must Use Continuous Integration

This is one of the tier 1 standards. See full list [on the overview page](README.md).

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
The existence of unit tests is highly encouraged as part of this standard, but not required. Since CI also tests the installation of your package, it can be set up without the existence of any unit tests.

See a guide on how to set up multiple CI options from the [STScI Training Library](https://spacetelescope.github.io/training-library/ci_testing.html#introduction-to-continuous-integration)

## Useful Links
- [Travis Tutorial](https://docs.travis-ci.com/user/tutorial/)
- [General information on CI by Thought Works](https://www.thoughtworks.com/continuous-integration)
- [General information on CI by Atlassian](https://www.atlassian.com/continuous-delivery/principles/continuous-integration-vs-delivery-vs-deployment)