# Create Octopus Release

A GitHub action to create the [octopus release](https://octopus.com/docs/octopus-rest-api/octopus-cli/create-release).

You could use:

- [albumprinter/actions-get-git-version](https://github.com/albumprinter/actions-get-git-version) to get the semver using git log
- [albumprinter/actions-pack-and-push-nuget](https://github.com/albumprinter/actions-pack-and-push-nuget) to pack and push a nuget package

## Usage

```yaml
  - uses: albumprinter/actions-create-octopus-release@v1
    with:
        project: OCTOPUS_PROJECT
        version: PACKAGE_VERSION or ${{ steps.git-version.outputs.version }}
        octopus-api: ${{ secrets.OCTOPUS_URL }}
        octopus-key: ${{ secrets.OCTOPUS_KEY }}
```
