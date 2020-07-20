# Project Must Have Documented Citation Information

This is one of the tier 2 standards. See full list [on the overview page](README.md).

## Short description

We require that the project documentation or repository contains a description of how to properly cite the project in publications and/or other software.

## Importance of this standard

Unlike journal articles, software repositories do not have a clear title page or list of authors.  Providing a citation description makes it easier for (and encourages) users to correctly cite your software in publications and acknowledgements.

## Options for this standard

We require that teams choose at least one of the following options:

- Include a `CITATION` file in the main directory of the repository that contains an appropriate description.
- Include an appropriate description in the repository's main `README` file.
- Include an appropriate description in the project's main documentation source (e.g. JDox, ReadTheDocs, etc.).

Though not required, another great way to make your software easily citable is to register the project with [Zenodo](https://zenodo.org/).  Zenodo is an open-access tool that allows users to upload software (and any accompanying data, reports, presentations, etc.) and receive a digital object identifier (DOI) for each submission.  For more information, visit https://about.zenodo.org/, and to sign up, visit https://zenodo.org/signup/.

## How to apply this standard

Teams may create a citation description that is best suited for their project.  Below, we provide an example description, taken from the [STScI Style Guides](https://github.com/spacetelescope/style-guides/blob/master/templates/CITATION):

```
If you use <package> for work/research presented in a publication (whether
directly, or as a dependency to another package), we recommend and encourage
the following acknowledgment:

  <add acknowledgement>

We encourage you to also include citations to the papers in the main text
wherever appropriate.

Recommended BibTeX entries for the above citations are:

@ARTICLE{<reference>,
   author = {authors},
    title = "title",
  journal = "journal",
 keywords = {keyword1, keyword2},
     year = 2019,
    month = jan,
   volume = 1,
      doi = {<thedoi>},
}
```

## Useful Links

- [STScI Style Guides Template for Citation](https://github.com/spacetelescope/style-guides/blob/master/templates/CITATION)
- [Zenodo](https://zenodo.org)