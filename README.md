# DEEP (Data Education & Exploration Project) [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/ricedatasci/deep/master)

This repository houses the website for DEEP as well as some convenience wrapper
code&trade; for the datasets used by groups in this project.

## mkdocs site

### adding content

This site uses [mkdocs](https://mkdocs.org) to generate a website from markdown
and jupyter notebooks.  To add a page to the site, simply put the markdown or
`.ipynb` file in a reasonable spot in the `docs` directory, and update
`mkdocs.yml` to include a path to your file:

```diff
nav:
  - Overview: index.md
  - Curriculum:
    - Git & Github: curriculum/git.md
    - Python:
      - Installation: curriculum/python/installation.md
      - Basics: curriculum/python/basics.ipynb
      - Exercise: curriculum/python/exercise.ipynb
    - Modeling:
+      - Linear Regression: curriculum/modeling/linear-regression.ipynb
+      - Linear Models: curriculum/modeling/linear-models.ipynb
  - Contributors: contributors.md
  - Acknowledgement: acknowledgement.md
```

### building site

Prepare local environment (ideally in a virtualenv)

```shell
$ pip install -r requirements.txt
$ pip install git+git://github.com/gvacaliuc/mknotebooks.git
```

Serve site locally:

```shell
$ mkdocs serve
```

Build site (outputs to `./site`):

```shell
$ mkdocs build
```
