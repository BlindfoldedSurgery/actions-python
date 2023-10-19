# actions-python

This repository contains a set of reusable workflows geared towards Python projects using Poetry.

The project follows semantic versioning. You can depend on tags for specific versions of use a
major version tag (e.g. `v1`).

Every commit on the main branch leads to a new release. Releases are managed by
[commitizen][commitizen], which relies on [conventional commits]. To make sure you don't
accidentally create commits with an unconventional message, install a pre-commit hook using
`make pre-commit`.

[commitizen]: https://commitizen-tools.github.io/commitizen/

[ccommit]: https://www.conventionalcommits.org/en/v1.0.0/

## Example

```yaml
jobs:
  lint:
    uses: BlindfoldedSurgery/actions-python/.github/workflows/lint.yml@v1
    with:
      python-version: '3.11'
```

## Available jobs

### lint

Lints a Poetry project using black, ruff and mypy.

**Inputs:**

| Name           | Required |  Default   |  Example   | Description                               |
|:---------------|:--------:|:----------:|:----------:|-------------------------------------------|
| python-version |   yes    |            |   `3.11`   | The Python version to use                 |
| debian-version |    no    | `bookworm` | `bullseye` | The Debian version name for the container |

### test

Runs unit tests for a project using pytest. Optionally collects and submits coverage report to
[codecov.io](https://codecov.io).

**Inputs:**

| Name            | Required |  Default   |    Example     | Description                                                                                   |
|:----------------|:--------:|:----------:|:--------------:|-----------------------------------------------------------------------------------------------|
| python-version  |   yes    |            |     `3.11`     | The Python version to use                                                                     |
| debian-version  |    no    | `bookworm` |   `bullseye`   | The Debian version name for the container                                                     |
| submit-coverage |    no    |  `false`   | `true`/`false` | Whether to collect and submit the coverage report. Requires the CODECOV_TOKEN secret as well. |

**Secrets:**

| Name            |           Required           | Description                                                 |
|:----------------|:----------------------------:|-------------------------------------------------------------|
| `CODECOV_TOKEN` | if `submit-coverage` is true | The codecov.io token to use for coverage report submission. |

### publish-package

Build a package using Poetry and publish it to a custom repository.

Example `poetry.toml`:

```toml
[repositories.pypi-bs]
url = " https://pypi.blindfolded.surgery/"
```

**Inputs:**

| Name           | Required |  Default   |     Example      | Description                                                  |
|:---------------|:--------:|:----------:|:----------------:|--------------------------------------------------------------|
| python-version |   yes    |            |      `3.11`      | The Python version to use                                    |
| debian-version |    no    | `bookworm` |    `bullseye`    | The Debian version name for the container                    |
| pypi-username  |   yes    |            | `mycoolusername` | The username for your custom pypi repository.                |
| repo-name      |    no    | `pypi-bs`  |                  | The repo name as configured in your project's `poetry.toml`. |

**Secrets:**

| Name            | Required | Description                                   |
|:----------------|:--------:|-----------------------------------------------|
| `pypi-password` |   yes    | The password for your custom pypi repository. |
