# Changelog

## v2.5.5 (2024-12-14)

### Fix

- **deps**: update dependency uv to v0.5.9

## v2.5.4 (2024-12-11)

### Fix

- **deps**: update dependency uv to v0.5.8

## v2.5.3 (2024-12-07)

### Fix

- **deps**: update dependency uv to v0.5.7

## v2.5.2 (2024-12-06)

### Fix

- **deps**: update dependency poetry to v1.8.5

## v2.5.1 (2024-12-05)

### Fix

- Use correct uv version

## v2.5.0 (2024-12-05)

### Feat

- Use setup action for uv

## v2.4.3 (2024-12-04)

### Fix

- Install all extras with uv

## v2.4.2 (2024-12-04)

### Fix

- Ensure pipx package are in PATH

## v2.4.1 (2024-12-04)

### Fix

- Install pipx before using it

## v2.4.0 (2024-12-04)

### Feat

- Support uv as build tool

## v2.3.0 (2024-12-03)

### Feat

- Update runner image to ubuntu-24.04

## v2.2.5 (2024-10-14)

### Fix

- **deps**: update dependency poetry to v1.8.4

## v2.2.4 (2024-10-07)

### Fix

- Ignore empty lines

## v2.2.3 (2024-10-07)

### Fix

- Revert base64 decoding change

## v2.2.2 (2024-10-07)

### Fix

- Explicitly request bash shell

## v2.2.1 (2024-10-07)

### Fix

- Decode env vars

## v2.2.0 (2024-10-07)

### Feat

- **test**: Accept env vars

## v2.1.3 (2024-10-06)

### Fix

- **deps**: update dependency pre-commit to v4

## v2.1.2 (2024-09-01)

### Fix

- Honor tests-selector if coverage is enabled

## v2.1.1 (2024-09-01)

### Fix

- Add missing dollar-sign in GitHub Actions expression

## v2.1.0 (2024-09-01)

### Feat

- Allow selecting specific tests for execution

### Fix

- Honor custom test location if no coverage is used

## v2.0.0 (2024-06-30)

### Feat

- Check formatting with ruff

## v1.3.2 (2024-05-10)

### Fix

- **test**: Upload Coverage reports in a separate job

## v1.3.1 (2024-04-06)

### Fix

- bump version on Poetry update

## v1.3.0 (2024-01-13)

### Feat

- Add input to customize lint path
- Add input to customize test location

## v1.2.1 (2023-11-11)

### Fix

- Revert usage of prebuilt Poetry image because of permission issues

## v1.2.0 (2023-11-11)

### Feat

- Use container image with prebuilt Poetry

## v1.1.1 (2023-10-28)

### Fix

- **ci**: Publish major tag
- **ci**: Reference workflow version
- **ci**: Reference actual reusable workflow
- **ci**: Use reusable workflow

## v1.1.0 (2023-10-21)

### Feat

- Introduce build-image-docker workflow

## v1.0.0 (2023-10-19)

Same as v0.5.1.

## v0.5.1 (2023-10-19)

### Fix

- Fix job name

## v0.5.0 (2023-10-19)

### Feat

- Add publish-package workflow

## v0.4.0 (2023-10-19)

### Feat

- Add test workflow

## v0.3.0 (2023-10-19)

### Feat

- Introduce major version tags

## v0.2.0 (2023-10-19)

### Feat

- configure commitizen

## 0.1.0

Initial version.
