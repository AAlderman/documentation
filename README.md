# OpenSAFELY Documentation

Documentation built using [mkdocs](https://www.mkdocs.org/).

includes [lots of very nice
customisations](https://squidfunk.github.io/mkdocs-material/reference/abbreviations/)
for formatting documentation.

View it at https://docs.opensafely.org

## Building locally and testing

- Create a virtual environment
- `pip install -r requirements.txt`
- `mkdocs serve`

To pull in the latest version of the cohortextractor docstrings run:

    pip-compile -P opensafely-cohort-extractor
    pip install -r requirements.txt

If you have added new functions you will need to add an explicit
reference to them in [docs/study-def-variables.md](./docs/study-def-variables.md).


## Deploying

The [docs site](https://docs.opensafely.org) is served by [readthedocs](https://readthedocs.org/), using a webhook to build the [latest version](https://readthedocs.org/projects/opensafely-documentation/versions/) from the `master` branch when it is updated. 

There are a [few redirects](https://readthedocs.org/dashboard/opensafely-documentation/redirects/) from old `stable` urls to current `latest` urls.

### Github Pages deployment

Previously, we would run mkdocs locally to compile the HTML, commit the output to a `gh-pages` branch and push to Github. This was all handled for us by running the command:

    mkdocs gh-deploy

Note: if you are deploying from a local environment for the first time, you may wish to set up the `gh-pages` branch before running mkdocs:

    % git checkout gh-pages
    Branch 'gh-pages' set up to track remote branch 'gh-pages' from 'origin'.
    Switched to a new branch 'gh-pages'
