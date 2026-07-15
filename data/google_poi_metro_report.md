# Metro-wide Google POI corrections — full validation report

## Anchor validation

- total anchors: **1677**
- valid anchors: **753**
- invalid anchors: **924**

### Invalid reasons

- matched_name_not_in_propagation: 349
- no_connection_to_X_network: 296
- no_road_within_150m: 279

## Edges

- total edge features emitted: **11503**
- corrected road segments (single_owner + split_halves): **11351**
  - single_owner: 10777
  - equal_split: 287
  - multi_quartier: 68
  - ambiguous: 57
  - blocked_barrier: 27
- total corrected road length: **674786.5 m**
- equal-split corridors (real components): **58**
- frontier midpoints: **287**
- ambiguous (isolated contested) edges: **57**
- multi-quartier edges: **68**
- blocked-by-barrier edges: **27**

## Top 20 quartier pairs by corrected road length

| A | B | corridor edges | total m | A share m | B share m |
|---|---|---:|---:|---:|---:|
| Vodjè-Centre | Vodjè-Finagnon | 10 | 1614.6 | 1264.5 | 350.1 |
| Fidjrossè-Centre | Fidjrossè-Kpota | 19 | 1462.0 | 756.7 | 705.3 |
| Finagnon | Tokplégbé | 6 | 1393.9 | 203.6 | 1190.3 |
| Ayélawadjè-Agongbomè | Sègbèya-Sud | 8 | 1313.1 | 533.1 | 780.0 |
| Gbégamey-Centre | Gbégamey-Dodo-Ayidjè | 14 | 1288.8 | 518.3 | 770.5 |
| Avotrou-Aïmonlonfidé | Avotrou-Gbègo | 7 | 1085.2 | 403.3 | 681.9 |
| Midombo | Sègbèya-Sud | 6 | 1012.6 | 588.9 | 423.7 |
| Gankpodo | Yénawa | 5 | 857.1 | 273.5 | 583.6 |
| Saint-Jean-Gbèdiga | Yévèdo | 4 | 836.6 | 392.3 | 444.3 |
| Cadjèhoun-Gare | Cadjèhoun-Kpota | 6 | 690.7 | 324.2 | 366.5 |
| Houéyihô | Védokô | 11 | 668.0 | 587.2 | 80.8 |
| Ayélawadjè | Misséssin | 3 | 653.0 | 464.9 | 188.1 |
| Kouhounou | Zogbo | 6 | 648.0 | 327.6 | 320.4 |
| Jéricho-Nord | Sèdjro-Saint-Michel | 7 | 638.9 | 96.9 | 542.1 |
| Gbéto | Zongo-Nima | 2 | 597.2 | 299.3 | 297.9 |
| Cadjèhoun-Azalokogon | Cadjèhoun-Kpota | 7 | 590.5 | 375.0 | 215.5 |
| Bocossi-Tokpa | Missèbô | 3 | 586.5 | 136.1 | 450.5 |
| Hindé-Sud | Jéricho-Nord | 2 | 584.9 | 196.5 | 388.4 |
| Kpondéhou | Sègbèya-Sud | 3 | 579.8 | 192.1 | 387.7 |
| Aïdjèdo | Jéricho-Nord | 4 | 567.2 | 246.3 | 320.9 |
