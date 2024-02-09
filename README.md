# Aeromancy project template

Copier template for Aeromancy-managed projects. This makes it easy to get a new
Aeromancy project up and running. This template (along with Aeromancy) is fairly
opinionated makes a lot of decisions for you in terms of workflows.

Template originally based on
[pdm-project/copier-pdm](https://github.com/pdm-project/copier-pdm).

## Requirements

This template requires the following dependencies:

- Python 3
- Git
- [Copier](https://copier.readthedocs.io/en/stable/)
- [PDM](https://pdm.fming.dev)

## Quick Start

1. Install [PDM](https://pdm.fming.dev) with
   [Copier](https://copier.readthedocs.io/en/stable/) support:

```bash
pip install --user "pdm[copier]"
```

2. Set up a new Aeromancy-managed project with this template: (this will create
   the project directory for you)

```bash
copier copy --trust "gh:quant-aq/aeromancy-project-template" <project_name>
```

3. Install project dependencies:

```bash
cd <project_name>
git init
pdm install --dev
```

4. Check out the `README.md` for more information or launch the doc server to
   see it in a browser:

```bash
pdm doc
```

## Template features

### Package manager

The template project uses [PDM](https://pdm.fming.dev), with a pre-defined
`pyproject.toml`.

### Documentation and changelog

- Documentation is built with [MkDocs](https://github.com/mkdocs/mkdocs)
  ([Material theme](https://github.com/squidfunk/mkdocs-material))

### Pre-commit and linter

[pre-commit](https://pre-commit.com/) is used for both commit hook and linting,
including the following hooks:

- [ruff](https://github.com/charliermarsh/ruff) (linting and formatting in
  [Black](https://github.com/psf/black) style)
- [keep-sorted](https://github.com/google/keep-sorted)
- [do-not-submit](https://github.com/jlebar/pre-commit-hooks/blob/master/check_do_not_submit.py)

### Tests

- Tests run with [pytest](https://pytest.org/). GitHub Actions provide matrix
  support.
