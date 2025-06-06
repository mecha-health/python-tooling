# {{cookiecutter.project_name}}

[![pre-commit](https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit&logoColor=white)](https://github.com/pre-commit/pre-commit)
[![Tests status][tests-badge]][tests-link]
[![Linting status][linting-badge]][linting-link]
[![Documentation status][documentation-badge]][documentation-link]
[![License][license-badge]](./LICENSE.md)

<!-- prettier-ignore-start -->
[tests-badge]:              {{cookiecutter.__repo_url}}/actions/workflows/tests.yml/badge.svg
[tests-link]:               {{cookiecutter.__repo_url}}/actions/workflows/tests.yml
[linting-badge]:            {{cookiecutter.__repo_url}}/actions/workflows/linting.yml/badge.svg
[linting-link]:             {{cookiecutter.__repo_url}}/actions/workflows/linting.yml
[documentation-badge]:      {{cookiecutter.__repo_url}}/actions/workflows/docs.yml/badge.svg
[documentation-link]:       {{cookiecutter.__repo_url}}/actions/workflows/docs.yml
{%- if cookiecutter.license == "MIT" %}
[license-badge]:            https://img.shields.io/badge/License-MIT-yellow.svg
{%- elif cookiecutter.license == "BSD-3" %}
[license-badge]:            https://img.shields.io/badge/License-BSD_3--Clause-blue.svg
{%- elif cookiecutter.license == "GPL-3.0" %}
[license-badge]:            https://img.shields.io/badge/License-GPLv3-blue.svg
{%- endif %}
<!-- prettier-ignore-end -->

{{cookiecutter.project_short_description}}

## About

## Getting Started

### Prerequisites

<!-- Any tools or versions of languages needed to run code. For example specific Python or Node versions. Minimum hardware requirements also go here. -->

`{{cookiecutter.project_slug}}` requires Python {{cookiecutter.min_python_version}}{% if cookiecutter.min_python_version != cookiecutter.max_python_version %}&ndash;{{cookiecutter.max_python_version}}{% endif %}.

### Installation

<!-- How to build or install the application. -->

We recommend installing in a project specific virtual environment created using
a environment management tool such as
[Conda](https://docs.conda.io/projects/conda/en/stable/). To install the latest
development version of `{{cookiecutter.project_slug}}` using `pip` in the currently active
environment run

```sh
pip install git+{{cookiecutter.__repo_url}}.git
```

Alternatively create a local clone of the repository with

```sh
git clone {{cookiecutter.__repo_url}}.git
```

and then install in editable mode by running

```sh
pip install -e .
```

### Running Locally

How to run the application on your local system.

### Running Tests

<!-- How to run tests on your local system. -->

Tests can be run across all compatible Python versions in isolated environments
using [`tox`](https://tox.wiki/en/latest/) by running

```sh
tox
```

To run tests manually in a Python environment with `pytest` installed run

```sh
pytest tests
```

again from the root of the repository.

### Building Documentation

The MkDocs HTML documentation can be built locally by running

```sh
tox -e docs
```

from the root of the repository. The built documentation will be written to
`site`.

Alternatively to build and preview the documentation locally, in a Python
environment with the optional `docs` dependencies installed, run

```sh
mkdocs serve
```

## Roadmap

- [x] Initial Research
- [ ] Minimum viable product <-- You are Here
- [ ] Alpha Release
- [ ] Feature-Complete Release
{%- if cookiecutter.funder != '' %}

## Acknowledgements

This work was funded by {{cookiecutter.funder}}.
{%- endif %}
