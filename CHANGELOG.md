# Changelog

Changes between model versions. Newest first.

## v6.1 (resource-catalogue 6.4)

Snapshot of the resource-catalogue service models. Compared with `archive/v6-converted-nodes`:

- **Java binding keys** (`bundleClass`, `bundlePayloadField`, `resourceClass`) are now part of every
  model except `conftemp`.
- **License URL autofill**: `license.licenseURL` has `form.autofillFrom`
  (`licenseName` -> SPDX vocabulary `extras.url`) in `guidelines`, `deployable`, `adapter` and `training`.
- **Federated dropdowns** now call the list endpoint with `?federation=true` and use
  `labelField: "label"` (name followed by the node PID in parentheses):
  - `rir`: `interoperabilityRecordIds` (`/api/interoperabilityRecord/list`)
  - `adapter`: `linkedResource.linkedResourceId` (`/api/rt_value/list`)
  - `training`: `eoscRelatedServices` (`/api/service/list`)
- Models `catalogue`, `organisation`, `service` and `datasource` are otherwise unchanged.

Not carried over: `m-b-con-igds`, `m-b-con-monitoring` and `m-b-con-probes` (no counterpart in the service).

## archive/v6-converted-nodes

Converted v6 models for the node-based catalogue, including `-v6c` models and `conftemp`/`rir`.

## Earlier versions

`archive/v6-converted`, `archive/v6`, `archive/v5` and `archive/configuration-templates` predate this changelog.
