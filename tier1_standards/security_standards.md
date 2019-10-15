# Software Must Meet Basic Security Standards

This is one of the tier 1 software standards. See full list [here](tier1_standards_overview.md)

## Short description
While certain applications require a more focus analysis of their security faults, all software products should follow the most basic security standards.

## Importance of standard
Basic security standards need to be met in order to protect unintended information from being released which can lead to vulnerabilities for you software, or even your organization as a whole.

## Options for this standard
Different tools will have different possibilities for security vulnerabilities, so it is up to the code owners to determine what the most relevant problems are. All tools should follow the STScI Style Guide's list of [information to never commit](https://github.com/spacetelescope/style-guides/blob/master/guides/security.md#secure-information). Software tools deemed to have more risks can also look into the [OWASP Top 10](https://www.owasp.org/index.php/Category:OWASP_Top_Ten_2017_Project) list of security risks and how to prevent them.  

## How to apply this standard
To meet the most basic security requirement of not committing sensitive information, you will need to:
 - Check your repository for any sensitive information that may have been committed. This includes usernames, passwords, tokens, etc.
 - If any sensitive information is found, remove it from the repository and immediately invalidate any tokens/passwords as they are no longer secure.
 - Consider cleaning out your `git` history to remove commits containing this sensitive information (e.g. changelogs). See [GitHub's documentation on removing secure information](https://help.github.com/en/articles/removing-sensitive-data-from-a-repository) for details on this process.
