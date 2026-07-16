# Metro v5 — coverage-driven propagation report

## Scope

Strictly Cotonou + Abomey-Calavi commune polygons. Roads geometrically clipped at the commune boundary.

## Graph pre-filter

- ways_kept: 23421
- ways_skipped_scope: 3106
- edges_dropped_water: 10

## Virtual connectors

- radius: 15 m · penalty: +25 m per connector
- selective (claimed-anchored only): 44 added

## Coverage

| commune | total | claimed | unclaimed |
|---|---:|---:|---:|
| ABOMEY-CALAVI | 99502 | 98928 | 574 |
| COTONOU | 15156 | 14980 | 176 |

## Anchors

- total: 1677 · valid: 740 · CONFIRM-eligible: 1
- POI corrections accepted: 1665 · rejected (chef-lieu conflict): 327

## Frontiers

- equal-split corridors: 388
- frontier midpoints: 903
- multi-quartier junction vertices: 118

## Invariants

- **OWNER_DISCONNECTED_ROAD_SEGMENTS**: 0
- **IN_SCOPE_UNCLAIMED_ROAD_SEGMENTS**: 750

## Fragmentation residuals

- OSM_GRAPH_FRAGMENTATION: 74
- WATER_OR_BRIDGE_BLOCK: 2
