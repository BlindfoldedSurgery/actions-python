# actions-python

This repository contains a set of reusable workflows geared towards Python projects using Poetry.

The project follows semantic versioning. You can depend on tags for specific versions of use a
major version tag (e.g. `v1`).

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
