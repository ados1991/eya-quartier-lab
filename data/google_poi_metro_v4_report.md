# Metro v4 — quality-preserving completion report

## Graph repair (Phase 1)

Chosen radius: **20.0 m** · 69 bridges added

See google_poi_metro_v4_repair_sweep_report.md for the per-radius sweep.

## Anchors

- total: 1677 · valid: 753 · CONFIRM-eligible: 474

## Chef-lieu protection (Rule 1)

- CHEF_LIEU_CONFLICT events: **339**

## Connectivity repair loop

- isolated components before: 465 · repaired: 223
  - EQUAL_SPLIT: 57
  - UNRESOLVED_STRIP: 222
  - REASSIGNED_TO_NEIGHBOUR: 166
  - MULTI_QUARTIER_STRIP: 24

## In-scope completion (Phase 2)

- MULTI_QUARTIER_REVIEW: 12
- ANNEX_TO_EXISTING_QUARTIER: 648
- EQUAL_SPLIT: 71
- ANNEX_AFTER_POI: 8

## Phase 3 — remaining unclaimed classification

- TRUE_MISSING_ANCHOR_REVIEW      : **0**
- GRAPH_FRAGMENTATION_UNRECOVERED : **86**

## Final invariants

- **OWNER_DISCONNECTED_ROAD_SEGMENTS**: 0
- **IN_SCOPE_UNCLAIMED_ROAD_SEGMENTS**: 3113

## Per-commune coverage

| commune | total | claimed | unclaimed |
|---|---:|---:|---:|
| ABOMEY-CALAVI | 99229 | 96603 | 2626 |
| COTONOU | 15336 | 14849 | 487 |
