[![EOSC Beyond Logo][eosc-logo]]()

# Dynamic Form Models

Versioned backup of the JSON form models used by the dynamic catalogue forms
([catalogue-ui](https://github.com/madgeek-arc/catalogue-ui)) and served by the
resource-catalogue.

The live copies of the models are in `resource-catalogue/resource-catalogue-service/src/main/resources/models`.
This repository keeps a snapshot of them for every released version, so any earlier form definition
can be recovered or compared.

## Layout

```
eosc-beyond/
  v6.1/                        current - models shipped with resource-catalogue 6.4
  archive/
    v6-converted-nodes/        previous version (-v6c suffix, node-based catalogue)
    v6-converted/              earlier v6 conversion
    v6/                        original v6 models (-v6 suffix)
    v5/                        legacy v5 models
    configuration-templates/   early configuration template models
  scratch/                     experiments, not releases
```

Every version folder has a `MANIFEST.md` with its status, source, model list and changes.

## Versions

| Folder | Status | Notes |
|---|---|---|
| `v6.1` | **current** | Snapshot of the resource-catalogue service models (release 6.4). See [CHANGELOG](CHANGELOG.md). |
| `archive/v6-converted-nodes` | superseded | Plain form definitions, no Java binding keys. |
| `archive/v6-converted` | superseded | Earlier conversion. |
| `archive/v6` | archived | |
| `archive/v5` | archived | |
| `archive/configuration-templates` | archived | |

## Model files

Models are named `m-b-<name>.json`: `adapter`, `catalogue`, `conftemp`, `datasource`, `deployable`,
`guidelines` (interoperability records), `organisation`, `rir` (resource interoperability records),
`service`, `training`.

Older folders add a suffix (`-v6`, `-v6c`). From `v6.1` on, files keep the plain `m-b-<name>.json` name,
exactly as in the resource-catalogue.

## Contributing

Publishing steps, naming rules and commit style are in [CONTRIBUTING.md](CONTRIBUTING.md).
To check the JSON locally: `find . -name '*.json' -not -path './.git/*' -exec jq empty {} +`.
A GitHub Action runs the same check on every push and pull request.

---

[eosc-logo]: https://eosc.eu/wp-content/uploads/2024/02/EOSC-Beyond-logo.png