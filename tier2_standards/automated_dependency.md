# Project Must Use an Automated Dependency Controller

This is one of the tier 2 standards. See full list [on the overview page](README.md).

## Short description

Automated dependency controllers are tools that automatically detect which of your third-party software dependencies are out of date, and automatically open a Pull Request with proposed changes.  These tools help prevent security volnerabilities and make developers aware of new updates to dependencies.

## Importance of this standard

Automated dependency controllers help ensure that your software is up-to-date with latest third-party dependencies (e.g. ``numpy``, ``astropy``, ``pytest``, etc.), thus helping your software to continue to be maintainable as the python software exosystem evolves.  Furthermore, these tools help ensure that your software is not susceptible to security volnorabilities, especially for web frameworks.  Lastly, having periodically-updated dependencies ensures that your software continues to be installable and usable by external users who may be using fresh software environments and installations.


## Options for this standard

While there are a number of options available, we reccommend [``dependabot``](https://dependabot.com/), which is native to GitHub (and thus free for all repositories), or [``pyup``](https://pyup.io) (free for public repositories).


## How to apply this standard

- For ``dependabot``, visit https://app.dependabot.com/auth/sign-up,  and follow the instructions to create an account and add your specific software repository.
- For ``pyup``, visit https://pyup.io/, and follow the instructions to create an account and add your specific software repositry.

## Useful Links

- The ``jwql`` repository serves as an example of a project using ``pyup``.  See the ``jwql`` ``pyup.yml`` configuration file as an example of a configuration file.
- Some example of dependabot