# Territorial evidence · OSM amenities (ODbL)

_Audit-only_: False · _Matched POIs_: 183 · _Chefs total_: 311 · _Chefs with evidence_: 119

## Scoring definitions

- `support_count` POIs in Q's territory labelled with Q
- `contradiction_count` POIs in Q's territory labelled with another quartier
- `external_support_count` POIs labelled Q sitting in another chef's territory
- `confidence_score = 1 − e^(−total_evidence / 3)`  (rises to 1)
- `over_expansion_score = contradict / (support + contradict + 1)`
- `under_claim_score = external / (support + external + 1)`
- `boundary_shift_score = √(over_expansion × under_claim)`
- Ranking score = score × confidence (so low-evidence chefs don't dominate)

## 1. Most likely OVER-EXPANDED quartiers (top 20)

*Their current territory contains many POIs labelled for others — boundary likely too LARGE.*

| # | Quartier | Support | Contradict | External | over_exp | conf | rank_score |
|---:|---|---:|---:|---:|---:|---:|---:|
| 1 | **Missogbé** | 0 | 3 | 0 | 0.72 | 0.63 | 0.454 |
| 2 | **Dota** | 0 | 3 | 0 | 0.72 | 0.63 | 0.454 |
| 3 | **Ahouansori-Towéta-Kpota** | 0 | 3 | 0 | 0.72 | 0.63 | 0.454 |
| 4 | **Dandji-Hokanmè** | 0 | 3 | 0 | 0.70 | 0.63 | 0.441 |
| 5 | **Mifongou** | 0 | 3 | 0 | 0.67 | 0.63 | 0.425 |
| 6 | **Ouéga-Tokpa** | 0 | 3 | 0 | 0.64 | 0.63 | 0.406 |
| 7 | **Hlacômey** | 0 | 2 | 1 | 0.63 | 0.63 | 0.398 |
| 8 | **Cité-les-Palmiers
** | 0 | 2 | 1 | 0.63 | 0.63 | 0.398 |
| 9 | **Védokô** | 0 | 1 | 5 | 0.46 | 0.86 | 0.397 |
| 10 | **Kindonou** | 3 | 3 | 0 | 0.42 | 0.86 | 0.362 |
| 11 | **Sètôvi** | 1 | 2 | 1 | 0.48 | 0.74 | 0.353 |
| 12 | **Fifonsi
** | 0 | 2 | 0 | 0.63 | 0.49 | 0.307 |
| 13 | **Tankpê-Yoho** | 0 | 2 | 0 | 0.63 | 0.49 | 0.307 |
| 14 | **Tokpa
** | 0 | 2 | 0 | 0.63 | 0.49 | 0.307 |
| 15 | **Agassa-Godomey** | 0 | 2 | 0 | 0.63 | 0.49 | 0.307 |
| 16 | **Gbénonkpô** | 0 | 2 | 0 | 0.63 | 0.49 | 0.307 |
| 17 | **Gbénonkpô** | 0 | 2 | 0 | 0.63 | 0.49 | 0.307 |
| 18 | **Kansounkpa** | 1 | 2 | 0 | 0.48 | 0.63 | 0.303 |
| 19 | **Vodjè-Ayidoté** | 0 | 2 | 0 | 0.59 | 0.49 | 0.288 |
| 20 | **Fandji
** | 0 | 2 | 0 | 0.59 | 0.49 | 0.288 |

## 2. Most likely UNDER-CLAIMED quartiers (top 20)

*POIs labelled with their name sit in other chefs' territory — boundary likely too SMALL.*

| # | Quartier | Support | Contradict | External | under_claim | conf | rank_score |
|---:|---|---:|---:|---:|---:|---:|---:|
| 1 | **Togba_Maria-Gléta** | 0 | 0 | 8 | 0.83 | 0.93 | 0.771 |
| 2 | **Espace-Saint** | 0 | 0 | 7 | 0.81 | 0.90 | 0.730 |
| 3 | **Gbéto** | 0 | 0 | 6 | 0.84 | 0.86 | 0.723 |
| 4 | **Védokô** | 0 | 1 | 5 | 0.81 | 0.86 | 0.701 |
| 5 | **Akpakpa-Dodomè** | 0 | 0 | 5 | 0.75 | 0.81 | 0.608 |
| 6 | **Cité-la-Victoire
** | 0 | 0 | 4 | 0.71 | 0.74 | 0.520 |
| 7 | **Agla-Petit-Château** | 0 | 1 | 3 | 0.64 | 0.74 | 0.473 |
| 8 | **Zoundja
** | 0 | 0 | 3 | 0.72 | 0.63 | 0.454 |
| 9 | **Zogbo** | 0 | 0 | 3 | 0.72 | 0.63 | 0.454 |
| 10 | **Cocotomey** | 3 | 0 | 4 | 0.49 | 0.90 | 0.442 |
| 11 | **Ladji** | 2 | 1 | 3 | 0.49 | 0.86 | 0.420 |
| 12 | **Xwlacôdji-Plage** | 0 | 0 | 3 | 0.64 | 0.63 | 0.406 |
| 13 | **Sèdjro-Saint-Michel** | 7 | 2 | 6 | 0.41 | 0.99 | 0.406 |
| 14 | **Midombo** | 0 | 1 | 2 | 0.63 | 0.63 | 0.398 |
| 15 | **Agori** | 0 | 1 | 2 | 0.63 | 0.63 | 0.398 |
| 16 | **Gbétagbo** | 1 | 1 | 2 | 0.48 | 0.74 | 0.353 |
| 17 | **Mènontin** | 4 | 0 | 3 | 0.37 | 0.90 | 0.331 |
| 18 | **Agbatô** | 0 | 0 | 2 | 0.63 | 0.49 | 0.307 |
| 19 | **Tokplégbé** | 0 | 0 | 2 | 0.63 | 0.49 | 0.307 |
| 20 | **Dénou
** | 0 | 0 | 2 | 0.63 | 0.49 | 0.307 |

## 3. Most likely SHIFTED quartiers (top 20)

*Both over_expanded AND under_claimed — boundary is in the wrong place, not just wrong size.*

| # | Quartier | over_exp | under_claim | shift | conf | rank_score |
|---:|---|---:|---:|---:|---:|---:|
| 1 | **Védokô** | 0.46 | 0.81 | 0.61 | 0.86 | 0.528 |
| 2 | **Agla-Petit-Château** | 0.38 | 0.64 | 0.49 | 0.74 | 0.361 |
| 3 | **Hlacômey** | 0.63 | 0.46 | 0.54 | 0.63 | 0.340 |
| 4 | **Sèdjro-Saint-Michel** | 0.25 | 0.41 | 0.32 | 0.99 | 0.315 |
| 5 | **Cité-les-Palmiers
** | 0.63 | 0.38 | 0.49 | 0.63 | 0.307 |
| 6 | **Midombo** | 0.38 | 0.63 | 0.49 | 0.63 | 0.307 |
| 7 | **Agori** | 0.38 | 0.63 | 0.49 | 0.63 | 0.307 |
| 8 | **Sètôvi** | 0.48 | 0.32 | 0.39 | 0.74 | 0.286 |
| 9 | **Ladji** | 0.18 | 0.49 | 0.30 | 0.86 | 0.257 |
| 10 | **Gbétagbo** | 0.24 | 0.48 | 0.34 | 0.74 | 0.252 |
| 11 | **Houèto** | 0.26 | 0.24 | 0.25 | 0.96 | 0.241 |
| 12 | **Sèdami** | 0.38 | 0.46 | 0.41 | 0.49 | 0.202 |
| 13 | **Plateau
** | 0.38 | 0.46 | 0.41 | 0.49 | 0.202 |
| 14 | **Guinkômey** | 0.38 | 0.46 | 0.41 | 0.49 | 0.202 |
| 15 | **Zogbadjè** | 0.07 | 0.18 | 0.11 | 0.97 | 0.110 |
| 16 | **Dandji-Hokanmè** | 0.70 | 0.00 | 0.00 | 0.63 | 0.000 |
| 17 | **Kowégbo** | 0.00 | 0.00 | 0.00 | 0.28 | 0.000 |
| 18 | **Ouéga-Tokpa** | 0.64 | 0.00 | 0.00 | 0.63 | 0.000 |
| 19 | **Minonkpô-Wologuèdè** | 0.00 | 0.38 | 0.00 | 0.28 | 0.000 |
| 20 | **Djoukpa-Togoudo
** | 0.38 | 0.00 | 0.00 | 0.28 | 0.000 |

## 4. Strongest TERRITORY TRANSFER candidates (top 20)

*Per (from → to) cluster, ranked by zone confidence (combines POI count × road length).*

| # | From | → | To | conf | POIs supporting | POIs contradicting | Road m | Google Maps |
|---:|---|:-:|---|---:|---:|---:|---:|---|
| 1 | Kindonou | → | **Mènontin** | **0.45** | 2 | 0 | 1311 | [open](https://www.google.com/maps/@6.389146,2.364780,18z) |
| 2 | Houèto | → | **Togba_Maria-Gléta** | **0.33** | 2 | 2 | 566 | [open](https://www.google.com/maps/@6.439698,2.309203,18z) |
| 3 | Fifonsi
 | → | **Agori** | **0.31** | 2 | 0 | 508 | [open](https://www.google.com/maps/@6.439050,2.326869,18z) |
| 4 | Ouéga-Tokpa | → | **Togba_Maria-Gléta** | **0.31** | 2 | 0 | 504 | [open](https://www.google.com/maps/@6.462786,2.306017,18z) |
| 5 | Agassa-Godomey | → | **Gbétagbo** | **0.28** | 2 | 0 | 442 | [open](https://www.google.com/maps/@6.545184,2.357088,18z) |
| 6 | Dota | → | **Gbéto** | **0.26** | 2 | 1 | 381 | [open](https://www.google.com/maps/@6.359349,2.428311,18z) |
| 7 | Hlacômey | → | **Agbatô** | **0.23** | 2 | 0 | 327 | [open](https://www.google.com/maps/@6.390621,2.441632,18z) |
| 8 | Agamandin | → | **Agla-Petit-Château** | **0.21** | 1 | 0 | 681 | [open](https://www.google.com/maps/@6.457785,2.356164,18z) |
| 9 | Fandji
 | → | **Espace-Saint** | **0.19** | 1 | 0 | 576 | [open](https://www.google.com/maps/@6.472885,2.348916,18z) |
| 10 | Sèdjro-Saint-Michel | → | **Gbéto** | **0.19** | 2 | 8 | 250 | [open](https://www.google.com/maps/@6.366567,2.427939,18z) |
| 11 | Agla-Petit-Château | → | **Agla-Les-Pylônes** | **0.19** | 1 | 0 | 550 | [open](https://www.google.com/maps/@6.380950,2.372661,18z) |
| 12 | Houèkè-Gbo | → | **Houèkè-Honou** | **0.18** | 1 | 0 | 493 | [open](https://www.google.com/maps/@6.497327,2.365231,18z) |
| 13 | Tokpa
 | → | **Cocotomey** | **0.17** | 1 | 0 | 476 | [open](https://www.google.com/maps/@6.389403,2.309672,18z) |
| 14 | Kindonou | → | **Mènontin** | **0.17** | 1 | 0 | 471 | [open](https://www.google.com/maps/@6.391751,2.361516,18z) |
| 15 | Tankpè-Tanmè | → | **Cité-la-Victoire
** | **0.17** | 1 | 0 | 448 | [open](https://www.google.com/maps/@6.426195,2.318485,18z) |
| 16 | Fidjrossè-Kpota | → | **Akôgbato** | **0.17** | 1 | 0 | 448 | [open](https://www.google.com/maps/@6.357749,2.358385,18z) |
| 17 | Dandji-Hokanmè | → | **Agla-Petit-Château** | **0.17** | 1 | 2 | 435 | [open](https://www.google.com/maps/@6.366786,2.485549,18z) |
| 18 | Tankpè-Tanmè | → | **Zogbadjè** | **0.16** | 1 | 0 | 415 | [open](https://www.google.com/maps/@6.427299,2.330694,18z) |
| 19 | Ahouansori-Towéta-Kpota | → | **Ladji** | **0.16** | 1 | 1 | 410 | [open](https://www.google.com/maps/@6.389916,2.430485,18z) |
| 20 | Houèto | → | **Togba_Maria-Gléta** | **0.15** | 1 | 0 | 396 | [open](https://www.google.com/maps/@6.435083,2.301572,18z) |

## Aggregate

- **119** / 311 chefs have any evidence
- **22** chefs have over_expansion_score ≥ 0.5
- **15** chefs have under_claim_score ≥ 0.5
- **12** chefs have boundary_shift_score ≥ 0.3
- **94** transfer candidate zones
  - ≥ 0.50 confidence : 0
  - 0.30 – 0.50 confidence : 4
  - 0.15 – 0.30 confidence : 19
  - < 0.15 (very weak) : 71

Each transfer candidate carries a Google-Maps link at street-level zoom. Manual review workflow: `osm_qev_review_workflow.html`

## Audit-only reminder

When this is run on Google data, all outputs are gitignored. Corrections are re-encoded as IGN/OSM edits before re-running the OSM-only propagation. No Google data ships in EYA.