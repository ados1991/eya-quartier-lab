# POI → propagation correction signal · OSM amenities (ODbL)

_Evidence radius_: **150 m** · _Node-cluster eps_: **50 m** · _Buffer_: 700 m · _Audit-only_: False

## Metro-wide node verdict

| Verdict | Nodes | % of claimed |
|---|---:|---:|
| **AGREE** (POI majority == current owner) | 203 | 0.3 % |
| **DISAGREE** (POI majority != current owner, candidate correction) | **123** | **0.2 %** |
| NO_EVIDENCE (no POI nearby) | 71225 | 99.5 % |
| **TOTAL** | 71551 | 100.0 % |

**Of nodes WITH POI evidence (326 = 0.5 % of claimed): 37.7 % disagree.**

## Correction zones (spatially contiguous DISAGREE clusters)

| Confidence | # zones |
|---|---:|
| HIGH (≥3 POIs + ≥2 nodes voting same flip) | 20 |
| MEDIUM (≥2 supporting POIs) | 47 |
| LOW (1 POI) | 12 |
| **TOTAL** | **79** |

## Top 20 HIGH/MEDIUM correction zones

| # | n_nodes | from | → | to | supp_POIs | Google Maps |
|---:|---:|---|---|---|---:|---|
| 0 | 7 | Hlacômey | → | Agbatô | 14 | [open](https://www.google.com/maps/@6.390131,2.441825,18z) |
| 1 | 7 | Ahouansori-Towéta-Kpota | → | Ladji | 16 | [open](https://www.google.com/maps/@6.389773,2.429404,18z) |
| 2 | 5 | Houèto | → | Togba_Maria-Gléta | 10 | [open](https://www.google.com/maps/@6.440652,2.309157,18z) |
| 3 | 4 | Houéyihô-Tannou | → | Védokô | 8 | [open](https://www.google.com/maps/@6.377481,2.389903,18z) |
| 4 | 3 | Gbénonkpô | → | Midombo | 3 | [open](https://www.google.com/maps/@6.371850,2.440814,18z) |
| 5 | 3 | Ahouansori-Towéta-Kpota | → | Ladji | 6 | [open](https://www.google.com/maps/@6.391126,2.430496,18z) |
| 6 | 3 | Dandji-Hokanmè | → | Tokplégbé | 3 | [open](https://www.google.com/maps/@6.366181,2.485697,18z) |
| 7 | 3 | Missogbé | → | Védokô | 6 | [open](https://www.google.com/maps/@6.378556,2.390136,18z) |
| 8 | 3 | Tchinangbégbo
 | → | Zogbadjè | 6 | [open](https://www.google.com/maps/@6.429958,2.338836,18z) |
| 9 | 3 | Agassa-Godomey | → | Gbétagbo | 6 | [open](https://www.google.com/maps/@6.544841,2.356691,18z) |
| 10 | 2 | Dota | → | Guinkômey | 2 | [open](https://www.google.com/maps/@6.360345,2.429710,18z) |
| 11 | 2 | Gbédokpo | → | Sèdjro-Saint-Michel | 5 | [open](https://www.google.com/maps/@6.365418,2.428871,18z) |
| 12 | 2 | Mifongou | → | Espace-Saint | 2 | [open](https://www.google.com/maps/@6.364916,2.427063,18z) |
| 13 | 2 | Lom-Nava | → | Akpakpa-Dodomè | 4 | [open](https://www.google.com/maps/@6.374374,2.453675,18z) |
| 14 | 2 | Dandji-Hokanmè | → | Tokplégbé | 2 | [open](https://www.google.com/maps/@6.365729,2.485924,18z) |
| 15 | 2 | Missogbé | → | Védokô | 4 | [open](https://www.google.com/maps/@6.379143,2.390059,18z) |
| 16 | 2 | Sètôvi | → | Védokô | 4 | [open](https://www.google.com/maps/@6.378128,2.389642,18z) |
| 17 | 2 | Fifonsi
 | → | Agori | 4 | [open](https://www.google.com/maps/@6.439477,2.326559,18z) |
| 18 | 2 | Fifonsi
 | → | Agori | 4 | [open](https://www.google.com/maps/@6.439663,2.327155,18z) |
| 19 | 2 | Houèto | → | Togba_Maria-Gléta | 4 | [open](https://www.google.com/maps/@6.439856,2.309465,18z) |

## Top 30 chefs by net territory delta (gain − lose)

| Chef-lieu | Gain (nodes) | Lose (nodes) | Net |
|---|---:|---:|---:|
| Togba_Maria-Gléta | +15 | -0 | +15 |
| Védokô | +14 | -0 | +14 |
| Agbatô | +12 | -0 | +12 |
| Hlacômey | +0 | -12 | -12 |
| Ladji | +12 | -0 | +12 |
| Ahouansori-Towéta-Kpota | +0 | -12 | -12 |
| Tokplégbé | +10 | -0 | +10 |
| Dandji-Hokanmè | +0 | -10 | -10 |
| Akpakpa-Dodomè | +10 | -0 | +10 |
| Houèto | +2 | -11 | -9 |
| Missogbé | +0 | -7 | -7 |
| Agori | +7 | -0 | +7 |
| Fifonsi
 | +0 | -7 | -7 |
| Zogbadjè | +7 | -0 | +7 |
| Tchinangbégbo
 | +0 | -7 | -7 |
| Gbétagbo | +7 | -0 | +7 |
| Agassa-Godomey | +0 | -7 | -7 |
| Lom-Nava | +0 | -6 | -6 |
| Dota | +0 | -5 | -5 |
| Mènontin | +5 | -0 | +5 |
| Kindonou | +0 | -5 | -5 |
| Guinkômey | +4 | -0 | +4 |
| Mifongou | +0 | -4 | -4 |
| Midombo | +4 | -0 | +4 |
| Gbénonkpô | +0 | -4 | -4 |
| Houéyihô-Tannou | +0 | -4 | -4 |
| Ouéga-Tokpa | +0 | -4 | -4 |
| Gbéto | +3 | -0 | +3 |
| Espace-Saint | +3 | -0 | +3 |
| Cadjèhoun-Aupiais | +3 | -0 | +3 |

## Methodology

1. For every currently-claimed road graph node (700 m buffered propagation), query all matched POIs within `evidence_radius = 150 m`.
2. Tally votes per quartier, weighted by match confidence (1.0 for FULL_HYPHEN, 0.85 for FULL_SINGLE_UNIQUE, 0.6 for TOKEN_UNIQUE).
3. Compare top-vote quartier to current propagation owner. AGREE / DISAGREE / NO_EVIDENCE.
4. Cluster DISAGREE nodes by spatial proximity + same proposed flip pair (from→to). Each cluster = one correction zone.
5. Confidence: HIGH if ≥3 supporting POIs and ≥2 nodes in the zone; MEDIUM if ≥2 POIs; LOW otherwise.

## Important

Google data (when used) remains audit-only. Corrections proposed here are reviewed by a human and re-encoded as IGN / OSM edits, after which the OSM-only propagation pipeline is re-run. No Google data ships in any final dataset.