# Aeromancy project template

[![Docs](https://img.shields.io/badge/Docs-yellow?style=flat&link=https%3A%2F%2Fquant-aq.github.io%2Faeromancy%2F)](https://quant-aq.github.io/aeromancy/)
[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)
[![pdm-managed](https://img.shields.io/badge/pdm-managed-blueviolet)](https://pdm.fming.dev)
[![Ruff](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/astral-sh/ruff/main/assets/badge/v2.json)](https://github.com/astral-sh/ruff)
[![pre-commit enabled](https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit&logoColor=white)](https://pre-commit.com/)
![Apache 2.0 licensed](https://img.shields.io/github/license/quant-aq/aeromancy)

This is a [Copier](https://copier.readthedocs.io/en/stable/) template for
getting a new [Aeromancy](https://github.com/quant-aq/aeromancy)-managed project
up and running quickly. If you're not familiar with Aeromancy, you'll want to
start with its [documentation](https://quant-aq.github.io/aeromancy/). This
template (along with Aeromancy) is fairly opinionated makes a lot of decisions
for you in terms of workflows.

The template will build stubs for all necessary Aeromancy components. The
initial setup creates a simple ML pipeline with three steps:

1. Load a dataset
2. Train a model on the dataset
3. Evaluate the model on the dataset

## Requirements

This template requires the following dependencies:

- [Python](https://python.org) (3.10+)
- [Git](https://git-scm.com/)

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
git init ; pdm install --dev --no-self
```

4. Check out [Aeromancy](https://quant-aq.github.io/aeromancy/) docs for more
   information!

## Template features

The template was originally based on
[pdm-project/copier-pdm](https://github.com/pdm-project/copier-pdm) with some
modifications in [dmcc/copier-pdm](https://github.com/dmcc/copier-pdm).

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
