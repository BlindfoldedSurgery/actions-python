# actions-python

This repository contains a set of reusable workflows geared towards Python projects using Poetry.

The project follows semantic versioning. You can depend on tags for specific versions of use a
major version tag (e.g. `v1`).

## lint

Lints a Poetry project using black, ruff and mypy.

**Inputs:**

| Name           | Required |  Default   |  Example   | Description                               |
|:---------------|:--------:|:----------:|:----------:|-------------------------------------------|
| python-version |   yes    |            |   `3.11`   | The Python version to use                 |
| debian-version |    no    | `bookworm` | `bullseye` | The Debian version name for the container |
