# Contributing

## Folder rules

- `eosc-beyond/vX.Y/` holds the current release. Only one version is current.
- When a new version is published, move the previous one to `eosc-beyond/archive/` and mark it
  superseded in its `MANIFEST.md` and in the README table.
- `eosc-beyond/scratch/` is for experiments. Nothing there is a release.

## File names

- Models are named `m-b-<name>.json`, matching the file in the resource-catalogue
  (`resource-catalogue-service/src/main/resources/models`). No version suffix in `vX.Y` folders.
- Do not rename files inside an existing version folder; they are a record of what was released.

## Publishing a version

1. Create `eosc-beyond/vX.Y/` and copy the models from the resource-catalogue.
2. Add a `MANIFEST.md` to the folder: status, source release, previous version, model list, changes.
3. Add an entry to `CHANGELOG.md` and update the version table in `README.md`.
4. Archive the previous version (`git mv` it under `eosc-beyond/archive/`).
5. Check the JSON locally: `find . -name '*.json' -not -path './.git/*' -exec jq empty {} +`
6. Commit: `chore: vX.Y models, updated according to resource-catalogue release A.B`.

## Commits

Short, imperative, optionally prefixed (`chore:`, `fix:`), as in the existing history.
