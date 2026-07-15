# Metro-wide Google POI corrections — v2 report (chef-lieu protection + connectivity invariant)

## Anchors

- total anchors: **1677**
- valid anchors: **753**
- CONFIRM+VALID (eligible to drive reassignment): **474**

## Chef-lieu protection (Rule 1)

- 150 m protection zone around every chef-lieu (298 chef-lieux)
- minimum corroboration inside protection zone: **3** CONFIRM anchors
- CHEF_LIEU_CONFLICT events (flips rejected in protection zones): **339**

## Connectivity invariant (Rule 2)

- iterations run: 3
- isolated components before repair: **476**
- isolated components repaired: **225**
- final disconnected roads (invariant violation): **0**

### Repair dispositions

- EQUAL_SPLIT: 57
- UNRESOLVED_DISCONNECTED: 231
- REASSIGNED_TO_NEIGHBOUR: 168
- MULTI_QUARTIER_REVIEW: 24

## Edges

- total edge features: **12745**
  - single_owner: 11188
  - equal_split: 760
  - blocked_barrier: 37
- total corrected road length: **493107.2 m**
- equal-split frontier midpoints: **760**

## Top 20 quartier pairs by corrected road length

| A | B | edges | total m | A share m | B share m |
|---|---|---:|---:|---:|---:|
| Djédjé-Layé | Gankpodo | 14 | 2624.3 | 1312.1 | 1312.1 |
| Cocotomey | Tokpa
 | 30 | 2133.1 | 1066.6 | 1066.6 |
| Gbégamey-Mifongou | Saint-Jean-Gbèdiga | 5 | 1656.7 | 828.3 | 828.3 |
| Guinkômey | Missèbô | 7 | 1415.3 | 707.7 | 707.7 |
| Djédjé-Layé | Yénawa | 7 | 1308.4 | 654.2 | 654.2 |
| Avotrou-Gbègo | Avotrou-Houézèkomè | 11 | 1305.0 | 652.5 | 652.5 |
| Midombo | Sègbèya-Sud | 12 | 1275.5 | 637.8 | 637.8 |
| Agbondjèdo | Minonkpô-Wologuèdè | 5 | 1274.2 | 637.1 | 637.1 |
| Djidjè | Djidjè-Aïchédji | 7 | 1262.3 | 631.1 | 631.1 |
| Kpondéhou | Sègbèya-Nord | 6 | 1248.4 | 624.2 | 624.2 |
| Avotrou-Gbègo | Suru-Léré | 8 | 1231.1 | 615.6 | 615.6 |
| Agbodjèdo | Minontchou | 10 | 1207.0 | 603.5 | 603.5 |
| Bocossi-Tokpa | Missèbô | 8 | 1171.7 | 585.8 | 585.8 |
| Kpankpan | Midombo | 12 | 1133.6 | 566.8 | 566.8 |
| Godomey-N'Gbèho | Hlazounto | 12 | 1131.2 | 565.6 | 565.6 |
| Dandji-Hokanmè | Finagnon | 7 | 1013.8 | 506.9 | 506.9 |
| Houéyihô | Vodjè-Ayidoté | 3 | 1011.7 | 505.8 | 505.8 |
| Mifongou | Sèdjro-Saint-Michel | 7 | 966.0 | 483.0 | 483.0 |
| Houèto | Tankpê-Yoho | 12 | 933.4 | 466.7 | 466.7 |
| Kouhounou | Mènontin | 8 | 890.7 | 445.4 | 445.4 |
