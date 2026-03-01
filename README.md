## Inputs

| Input | Required | Default | Description |
|---|---|---|---|
| `composer-install` | No | `true` | Whether to install Composer dependencies. |
| `directory-name` | No | Repository name | Name of the directory created inside the zip, and used as the base of the zip file name. |

## Example Workflow

```yaml
name: Create Release Zip
on:
  # Triggers when a new release is published.
  release:
    types: [published]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: ashleyfae/action-build-release-zip@main
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```
