# Metro v3 — in-scope completion report

## Anchors

- total: **1677** · valid: **753** · CONFIRM+VALID: **474**

## Graph fragmentation repair

- virtual bridge edges added: **37**

## Chef-lieu protection (Rule 1)

- 150 m protection zone · MIN_CORROBORATION = 3
- CHEF_LIEU_CONFLICT events: **339**

## Connectivity invariant repair loop

- isolated components before: **470**
- isolated components repaired: **224**
  - EQUAL_SPLIT: 57
  - UNRESOLVED_STRIP: 226
  - REASSIGNED_TO_NEIGHBOUR: 167
  - MULTI_QUARTIER_STRIP: 24

## In-scope completion pass (v3 new)

- MULTI_REVIEW: 12
- ONE_ELIGIBLE: 647
- MISSING_CHEF_LIEU: 75
- EQUAL_SPLIT: 71
- ONE_AFTER_POI: 8
- MISSING_CHEF_LIEU_POST_CONNECTIVITY: 76
- MISSING_CHEF_LIEU_CANDIDATE components: **151**
- MULTI_QUARTIER_REVIEW components: **12**

## Final invariants

- **IN_SCOPE_UNCLAIMED_ROAD_SEGMENTS**: 1173
- **OWNER_DISCONNECTED_ROAD_SEGMENTS**: 0

## Per-commune coverage

| commune | total | claimed | unclaimed |
|---|---:|---:|---:|
| ABOMEY-CALAVI | 99229 | 98236 | 993 |
| COTONOU | 15336 | 15156 | 180 |

## Out-of-scope excluded

- OUT_OF_SCOPE vertices (Sô-Ava, Ouidah, other communes): **38094**

