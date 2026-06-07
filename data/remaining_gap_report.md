# Remaining-gap audit — 700 m buffered competitive Dijkstra

_Buffer_: **700 m** spill-over · _Cluster eps_: **80 m** · _Min cluster_: **4** nodes

## Coverage

| Quantity | Value |
|---|---:|
| Total road graph nodes | 94,213 |
| Claimed at 700 m | 71,551 (75.9 %) |
| Unclaimed | 730 (0.8 %) |
| Unclaimed in audited clusters | 619 (84.8 % of unclaimed) |
| Audited clusters | 46 |

## Classification breakdown

| Bucket | Clusters | Nodes | Road km |
|---|---:|---:|---:|
| OSM graph fragmentation | 11 | 96 | 2.71 |
| Missing bridge crossing | 3 | 56 | 2.12 |
| Water-isolated pocket | 20 | 287 | 9.78 |
| Missing chef-lieu coverage | 9 | 154 | 5.18 |
| Administrative ambiguity | 0 | 0 | 0.00 |
| Legitimate no-quartier area | 0 | 0 | 0.00 |
| Unknown | 3 | 26 | 0.84 |
| **TOTAL** | **46** | **619** | **20.64** |

## Data vs algorithm

| Class | Clusters | Nodes | % of clustered nodes |
|---|---:|---:|---:|
| **DATA** (OSM frag · water pocket · missing chef · legit) | 40 | 537 | 86.8 % |
| **ALGORITHM** (missing bridge · admin ambiguity) | 3 | 56 | 9.0 % |
| Unknown | 3 | 26 | 4.2 % |

**Verdict: primarily a DATA problem.** Algorithm tuning will not close these gaps. Stop refining propagation and move to frontier skeleton generation.

## Top 10 largest clusters per bucket

### OSM graph fragmentation

| # | n | road m | commune | arrondissement | near chef (same) | dist m | water | bridge | comp |
|---|---:|---:|---|---|---|---:|:-:|:-:|---:|
| 8 | 19 | 626 | Abomey-Calavi (buffer) | Ouidah / Pahou | Cococodji | 4323 | Y | n | 20 |
| 13 | 12 | 337 | Abomey-Calavi | Abomey-Calavi / Godomey | Ganganzounmè
 | 528 | n | n | 12 |
| 16 | 11 | 332 | Abomey-Calavi | Abomey-Calavi / Akassato | Houèkè-Gbo | 3928 | Y | Y | 3 |
| 20 | 10 | 198 | Cotonou | Cotonou / Cotonou 3 | Agbodjèdo | 517 | n | Y | 6 |
| 24 | 8 | 355 | Abomey-Calavi | Abomey-Calavi / Kpanroun | Bozoun | 1847 | n | n | 12 |
| 25 | 8 | 181 | Abomey-Calavi | Abomey-Calavi / Calavi | Zoundja
 | 1233 | n | n | 10 |
| 27 | 8 | 221 | Abomey-Calavi (buffer) | Zè / Tangbo-Djèvié | Djissoukpa | 1504 | n | n | 8 |
| 28 | 7 | 130 | Abomey-Calavi | Abomey-Calavi / Kpanroun | Avagbé | 2274 | n | n | 7 |
| 37 | 5 | 92 | Abomey-Calavi | Abomey-Calavi / Zinvié | Kpotomey | 3056 | n | n | 5 |
| 41 | 4 | 155 | Abomey-Calavi | Abomey-Calavi / Kpanroun | Bozoun | 2226 | n | n | 12 |

### Missing bridge crossing

| # | n | road m | commune | arrondissement | near chef (same) | dist m | water | bridge | comp |
|---|---:|---:|---|---|---|---:|:-:|:-:|---:|
| 4 | 33 | 1508 | Abomey-Calavi | Abomey-Calavi / Godomey | Sèdjannako
 | 460 | Y | Y | 90099 |
| 14 | 12 | 340 | Abomey-Calavi (buffer) | So-Ava / So-Ava | Houèkè-Gbo | 4544 | Y | Y | 63 |
| 17 | 11 | 277 | Abomey-Calavi (buffer) | Ouidah / Pahou | Djèkpota | 2518 | Y | Y | 90099 |

### Water-isolated pocket

| # | n | road m | commune | arrondissement | near chef (same) | dist m | water | bridge | comp |
|---|---:|---:|---|---|---|---:|:-:|:-:|---:|
| 1 | 50 | 2047 | Abomey-Calavi | Abomey-Calavi / Zinvié | Gbodjè | 3485 | Y | n | 90 |
| 2 | 39 | 1647 | Abomey-Calavi (buffer) | So-Ava / Ganvié II | Houèkè-Gbo | 3597 | Y | n | 62 |
| 3 | 35 | 905 | Abomey-Calavi (buffer) | So-Ava / Ahomè-Lokpo | Gbodjè | 3990 | Y | n | 36 |
| 5 | 25 | 1097 | Abomey-Calavi | Abomey-Calavi / Akassato | Akassato | 3891 | Y | n | 43 |
| 6 | 23 | 558 | Abomey-Calavi (buffer) | Adjohoun / Togbota | Bozoun | 4117 | Y | n | 123 |
| 7 | 22 | 482 | Abomey-Calavi | Abomey-Calavi / Zinvié | Gbodjè | 2418 | Y | n | 90 |
| 18 | 11 | 574 | Abomey-Calavi | Abomey-Calavi / Akassato | Akassato | 4344 | Y | n | 43 |
| 19 | 10 | 368 | Abomey-Calavi | Abomey-Calavi / Akassato | Houèkè-Gbo | 3722 | Y | n | 62 |
| 22 | 10 | 327 | Abomey-Calavi | Abomey-Calavi / Akassato | Agassa-Godomey | 4696 | Y | n | 40 |
| 26 | 8 | 260 | Abomey-Calavi (buffer) | So-Ava / Ahomè-Lokpo | Agassa-Godomey | 4770 | Y | n | 40 |

### Missing chef-lieu coverage

| # | n | road m | commune | arrondissement | near chef (same) | dist m | water | bridge | comp |
|---|---:|---:|---|---|---|---:|:-:|:-:|---:|
| 0 | 75 | 2064 | Abomey-Calavi | Abomey-Calavi / Akassato | Agassa-Godomey | 4123 | n | n | 90099 |
| 9 | 16 | 596 | Abomey-Calavi | Abomey-Calavi / Kpanroun | Bozoun | 2117 | n | n | 34 |
| 10 | 13 | 606 | Abomey-Calavi | Abomey-Calavi / Kpanroun | Bozoun | 1758 | n | n | 34 |
| 11 | 13 | 496 | Abomey-Calavi (buffer) | Tori-Bossito / Avamè | Dassèkomey | 2782 | n | n | 37 |
| 12 | 12 | 406 | Abomey-Calavi | Abomey-Calavi / Akassato | Glo-Tokpa | 4375 | n | Y | 90099 |
| 23 | 9 | 397 | Abomey-Calavi (buffer) | Tori-Bossito / Avamè | Dassèkomey | 2575 | n | n | 90099 |
| 31 | 6 | 234 | Abomey-Calavi | Abomey-Calavi / Zinvié | Gbodjè | 2424 | n | n | 90099 |
| 35 | 5 | 200 | Abomey-Calavi | Abomey-Calavi / Zinvié | Gbodjè | 1526 | n | n | 90099 |
| 40 | 5 | 183 | Abomey-Calavi | Abomey-Calavi / Zinvié | Gbodjè | 2730 | n | n | 90099 |

### Unknown

| # | n | road m | commune | arrondissement | near chef (same) | dist m | water | bridge | comp |
|---|---:|---:|---|---|---|---:|:-:|:-:|---:|
| 15 | 11 | 359 | Abomey-Calavi | Abomey-Calavi / Zinvié | Gbodjè | 996 | n | Y | 90099 |
| 21 | 10 | 285 | Abomey-Calavi (buffer) | Zè / Yokpo | Houégoudo
 | 1140 | n | n | 90099 |
| 36 | 5 | 199 | Abomey-Calavi | Abomey-Calavi / Zinvié | Gbodjè | 955 | n | n | 90099 |

## Methodology

- **Propagation**: same 700 m commune-buffered Dijkstra as the current lab layer (`competitive_road_propagation_commune_buf700_full`).
- **Cluster**: single-link DBSCAN on unclaimed node centroids with `eps = 80 m`. Clusters smaller than `4` nodes are dropped as noise.
- **Road length**: sum of edge lengths between unclaimed nodes of the same cluster (each edge once).
- **Nearest chefs**: KD-tree lookup over all chefs of Cotonou + Abomey-Calavi. "Nearest" is great-circle distance from cluster centroid to chef-lieu point — not road distance, which is undefined for an unclaimed cluster by construction.
- **Water separation**: does the straight line from centroid to the nearest same-commune chef cross any major water polygon (canal/river/stream/natural=water/basin/reservoir)?
- **Bridge present**: any OSM `bridge=yes`/`cantilever` way passes within `80 m` of any cluster node.
- **Graph component size**: size of the road graph component the cluster sits in (union-find over the full adj).

## Classification rules (evaluated in order)

1. **OSM graph fragmentation** — graph component ≤ `20` nodes.
2. **Missing bridge crossing** — water separation AND bridge present near the cluster.
3. **Water-isolated pocket** — water separation AND no bridge.
4. **Missing chef-lieu coverage** — nearest same-commune chef > `1500 m` (or absent).
5. **Administrative ambiguity** — centroid within `200 m` of the strict commune boundary AND both communes have a chef within `800 m`.
6. **Legitimate no-quartier area** — cluster ≤ `8` nodes AND nearest same-commune chef > `1200 m`.
7. **Unknown** — none of the above.
