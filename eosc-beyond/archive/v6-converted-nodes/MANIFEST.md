# v6-converted-nodes

- **Status:** superseded by `v6.1`
- **Previous version:** `archive/v6-converted`
- **Naming:** `-v6c` suffix (`conftemp` and `rir` have none)

## Models (13)

adapter, catalogue, conftemp, con-igds, con-monitoring, con-probes, datasource, deployable, guidelines,
organisation, rir, service, training.

## Changes against `v6-converted`

All 13 files differ. In the models checked (`service`, `training`), the `nodePID` field changes from a
vocabulary dropdown backed by the federated-search `/api/nodes` endpoint to a plain string field with
`cssClasses: "uk-disabled"`, i.e. read-only in the form. The remaining models were not compared one by one.
