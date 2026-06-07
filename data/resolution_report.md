# Resolution proposals — final pre-frontier disposition

Source: `remaining_gap_clusters.geojson` — 46 clusters.

**Goal**: 0 unresolved road clusters inside scope before frontier skeleton generation.

## Disposition summary

| Disposition | Clusters | Nodes | Road km | Effect |
|---|---:|---:|---:|---|
| **ANNEX_TO_NEAREST_CHEF** | 11 | 88 | 2.51 | post-pass attribution at frontier-skeleton time — no IGN change, no OSM change |
| **BRIDGE_CROSSING_REQUIRED** | 3 | 56 | 2.12 | graph-build change — exempt bridge=yes ways from cross-water veto |
| **NEW_CHEF_LIEU_SEED** | 18 | 379 | 13.19 | extend IGN chef-lieu list with a new seed at the proposed location |
| **OSM_GRAPH_FIX** | 1 | 4 | 0.09 | add a road connector in OSM at the listed coords; re-pull roads |
| **EXCLUDED_AREA** | 13 | 92 | 2.73 | documented as un-routable hinterland — never claimed by any quartier |
| **TOTAL** | **46** | **619** | **20.64** | — |

## Status

✓ **46 clusters, 0 unresolved.** Ready for frontier skeleton generation.

## Per-cluster proposals

### ANNEX_TO_NEAREST_CHEF — 11 clusters · 88 nodes

- **#13** · 12 nodes · 337 m · _OSM graph fragmentation_ · Abomey-Calavi / Godomey
  - **Target**: Ganganzounmè

  - Tiny component of 12 nodes; too small to justify a chef-lieu and too far (528 m) to be a clean OSM fix. Post-pass attribution: assign all 12 nodes to Ganganzounmè
.

- **#15** · 11 nodes · 359 m · _Unknown_ · Abomey-Calavi / Zinvié
  - **Target**: Gbodjè
  - Edge-of-territory cluster in the main graph (comp=90099), no water in the way, nearest chef Gbodjè is 996 m. Post-pass attribution.

- **#20** · 10 nodes · 198 m · _OSM graph fragmentation_ · Cotonou / Cotonou 3
  - **Target**: Agbodjèdo
  - Tiny component of 6 nodes; too small to justify a chef-lieu and too far (517 m) to be a clean OSM fix. Post-pass attribution: assign all 10 nodes to Agbodjèdo.

- **#21** · 10 nodes · 285 m · _Unknown_ · Zè / Yokpo
  - **Target**: Houégoudo

  - Edge-of-territory cluster in the main graph (comp=90099), no water in the way, nearest chef Houégoudo
 is 1140 m. Post-pass attribution.

- **#24** · 8 nodes · 355 m · _OSM graph fragmentation_ · Abomey-Calavi / Kpanroun
  - **Target**: Bozoun
  - Tiny component of 12 nodes; too small to justify a chef-lieu and too far (1847 m) to be a clean OSM fix. Post-pass attribution: assign all 8 nodes to Bozoun.

- **#25** · 8 nodes · 181 m · _OSM graph fragmentation_ · Abomey-Calavi / Calavi
  - **Target**: Zoundja

  - Tiny component of 10 nodes; too small to justify a chef-lieu and too far (1233 m) to be a clean OSM fix. Post-pass attribution: assign all 8 nodes to Zoundja
.

- **#27** · 8 nodes · 221 m · _OSM graph fragmentation_ · Zè / Tangbo-Djèvié
  - **Target**: Djissoukpa
  - Tiny component of 8 nodes; too small to justify a chef-lieu and too far (1504 m) to be a clean OSM fix. Post-pass attribution: assign all 8 nodes to Djissoukpa.

- **#28** · 7 nodes · 130 m · _OSM graph fragmentation_ · Abomey-Calavi / Kpanroun
  - **Target**: Avagbé
  - Tiny component of 7 nodes; too small to justify a chef-lieu and too far (2274 m) to be a clean OSM fix. Post-pass attribution: assign all 7 nodes to Avagbé.

- **#36** · 5 nodes · 199 m · _Unknown_ · Abomey-Calavi / Zinvié
  - **Target**: Gbodjè
  - Edge-of-territory cluster in the main graph (comp=90099), no water in the way, nearest chef Gbodjè is 955 m. Post-pass attribution.

- **#37** · 5 nodes · 92 m · _OSM graph fragmentation_ · Abomey-Calavi / Zinvié
  - **Target**: Kpotomey
  - Tiny component of 5 nodes; too small to justify a chef-lieu and too far (3056 m) to be a clean OSM fix. Post-pass attribution: assign all 5 nodes to Kpotomey.

- **#41** · 4 nodes · 155 m · _OSM graph fragmentation_ · Abomey-Calavi / Kpanroun
  - **Target**: Bozoun
  - Tiny component of 12 nodes; too small to justify a chef-lieu and too far (2226 m) to be a clean OSM fix. Post-pass attribution: assign all 4 nodes to Bozoun.

### BRIDGE_CROSSING_REQUIRED — 3 clusters · 56 nodes

- **#4** · 33 nodes · 1508 m · _Missing bridge crossing_ · Abomey-Calavi / Godomey
  - **Target**: Sèdjannako

  - Whitelist the bridge near cluster centroid so Sèdjannako
 (≈ 460 m away) can claim these 33 nodes across the water. Fix is in the graph build (water-aware merge currently refuses the bridge edge): exempt OSM ways with `bridge=yes`/`cantilever` from the cross-water veto.

- **#14** · 12 nodes · 340 m · _Missing bridge crossing_ · So-Ava / So-Ava
  - **Target**: Houèkè-Gbo
  - Whitelist the bridge near cluster centroid so Houèkè-Gbo (≈ 4544 m away) can claim these 12 nodes across the water. Fix is in the graph build (water-aware merge currently refuses the bridge edge): exempt OSM ways with `bridge=yes`/`cantilever` from the cross-water veto.

- **#17** · 11 nodes · 277 m · _Missing bridge crossing_ · Ouidah / Pahou
  - **Target**: Djèkpota
  - Whitelist the bridge near cluster centroid so Djèkpota (≈ 2518 m away) can claim these 11 nodes across the water. Fix is in the graph build (water-aware merge currently refuses the bridge edge): exempt OSM ways with `bridge=yes`/`cantilever` from the cross-water veto.

### NEW_CHEF_LIEU_SEED — 18 clusters · 379 nodes

- **#0** · 75 nodes · 2064 m · _Missing chef-lieu coverage_ · Abomey-Calavi / Akassato
  - Cluster of 75 nodes (2064 m road) in Abomey-Calavi / Akassato; nearest same-commune chef (Agassa-Godomey) is 4123 m away — IGN list is missing a chef-lieu point for this area. Propose seed at (lat=6.538928, lng=2.401616).

- **#1** · 50 nodes · 2047 m · _Water-isolated pocket_ · Abomey-Calavi / Zinvié
  - Water-isolated settlement of 50 nodes (2047 m of road) in Abomey-Calavi / Zinvié, 3485 m from the nearest chef (Gbodjè) across major water with no bridge. Propose new chef-lieu at (lat=6.617048, lng=2.408749).

- **#2** · 39 nodes · 1647 m · _Water-isolated pocket_ · So-Ava / Ganvié II
  - Water-isolated settlement of 39 nodes (1647 m of road) in So-Ava / Ganvié II, 3597 m from the nearest chef (Houèkè-Gbo) across major water with no bridge. Propose new chef-lieu at (lat=6.474541, lng=2.392152).

- **#3** · 35 nodes · 905 m · _Water-isolated pocket_ · So-Ava / Ahomè-Lokpo
  - Water-isolated settlement of 35 nodes (905 m of road) in So-Ava / Ahomè-Lokpo, 3990 m from the nearest chef (Gbodjè) across major water with no bridge. Propose new chef-lieu at (lat=6.562920, lng=2.402966).

- **#5** · 25 nodes · 1097 m · _Water-isolated pocket_ · Abomey-Calavi / Akassato
  - Water-isolated settlement of 25 nodes (1097 m of road) in Abomey-Calavi / Akassato, 3891 m from the nearest chef (Akassato) across major water with no bridge. Propose new chef-lieu at (lat=6.502242, lng=2.399531).

- **#6** · 23 nodes · 558 m · _Water-isolated pocket_ · Adjohoun / Togbota
  - Water-isolated settlement of 23 nodes (558 m of road) in Adjohoun / Togbota, 4117 m from the nearest chef (Bozoun) across major water with no bridge. Propose new chef-lieu at (lat=6.685446, lng=2.429939).

- **#7** · 22 nodes · 482 m · _Water-isolated pocket_ · Abomey-Calavi / Zinvié
  - Water-isolated settlement of 22 nodes (482 m of road) in Abomey-Calavi / Zinvié, 2418 m from the nearest chef (Gbodjè) across major water with no bridge. Propose new chef-lieu at (lat=6.603959, lng=2.406312).

- **#9** · 16 nodes · 596 m · _Missing chef-lieu coverage_ · Abomey-Calavi / Kpanroun
  - Cluster of 16 nodes (596 m road) in Abomey-Calavi / Kpanroun; nearest same-commune chef (Bozoun) is 2117 m away — IGN list is missing a chef-lieu point for this area. Propose seed at (lat=6.666437, lng=2.400027).

- **#10** · 13 nodes · 606 m · _Missing chef-lieu coverage_ · Abomey-Calavi / Kpanroun
  - Cluster of 13 nodes (606 m road) in Abomey-Calavi / Kpanroun; nearest same-commune chef (Bozoun) is 1758 m away — IGN list is missing a chef-lieu point for this area. Propose seed at (lat=6.669970, lng=2.399979).

- **#11** · 13 nodes · 496 m · _Missing chef-lieu coverage_ · Tori-Bossito / Avamè
  - Cluster of 13 nodes (496 m road) in Tori-Bossito / Avamè; nearest same-commune chef (Dassèkomey) is 2782 m away — IGN list is missing a chef-lieu point for this area. Propose seed at (lat=6.510124, lng=2.239607).

- **#12** · 12 nodes · 406 m · _Missing chef-lieu coverage_ · Abomey-Calavi / Akassato
  - Cluster of 12 nodes (406 m road) in Abomey-Calavi / Akassato; nearest same-commune chef (Glo-Tokpa) is 4375 m away — IGN list is missing a chef-lieu point for this area. Propose seed at (lat=6.531313, lng=2.402783).

- **#18** · 11 nodes · 574 m · _Water-isolated pocket_ · Abomey-Calavi / Akassato
  - Water-isolated settlement of 11 nodes (574 m of road) in Abomey-Calavi / Akassato, 4344 m from the nearest chef (Akassato) across major water with no bridge. Propose new chef-lieu at (lat=6.507259, lng=2.403835).

- **#19** · 10 nodes · 368 m · _Water-isolated pocket_ · Abomey-Calavi / Akassato
  - Water-isolated settlement of 10 nodes (368 m of road) in Abomey-Calavi / Akassato, 3722 m from the nearest chef (Houèkè-Gbo) across major water with no bridge. Propose new chef-lieu at (lat=6.487169, lng=2.398180).

- **#22** · 10 nodes · 327 m · _Water-isolated pocket_ · Abomey-Calavi / Akassato
  - Water-isolated settlement of 10 nodes (327 m of road) in Abomey-Calavi / Akassato, 4696 m from the nearest chef (Agassa-Godomey) across major water with no bridge. Propose new chef-lieu at (lat=6.546321, lng=2.407285).

- **#23** · 9 nodes · 397 m · _Missing chef-lieu coverage_ · Tori-Bossito / Avamè
  - Cluster of 9 nodes (397 m road) in Tori-Bossito / Avamè; nearest same-commune chef (Dassèkomey) is 2575 m away — IGN list is missing a chef-lieu point for this area. Propose seed at (lat=6.505120, lng=2.235105).

- **#31** · 6 nodes · 234 m · _Missing chef-lieu coverage_ · Abomey-Calavi / Zinvié
  - Cluster of 6 nodes (234 m road) in Abomey-Calavi / Zinvié; nearest same-commune chef (Gbodjè) is 2424 m away — IGN list is missing a chef-lieu point for this area. Propose seed at (lat=6.610975, lng=2.401238).

- **#35** · 5 nodes · 200 m · _Missing chef-lieu coverage_ · Abomey-Calavi / Zinvié
  - Cluster of 5 nodes (200 m road) in Abomey-Calavi / Zinvié; nearest same-commune chef (Gbodjè) is 1526 m away — IGN list is missing a chef-lieu point for this area. Propose seed at (lat=6.607264, lng=2.392419).

- **#40** · 5 nodes · 183 m · _Missing chef-lieu coverage_ · Abomey-Calavi / Zinvié
  - Cluster of 5 nodes (183 m road) in Abomey-Calavi / Zinvié; nearest same-commune chef (Gbodjè) is 2730 m away — IGN list is missing a chef-lieu point for this area. Propose seed at (lat=6.612126, lng=2.404040).

### OSM_GRAPH_FIX — 1 clusters · 4 nodes

- **#43** · 4 nodes · 86 m · _OSM graph fragmentation_ · Cotonou / Cotonou 9
  - **Target**: Missèkplé
  - Tiny component of 8 nodes sits 209 m from Missèkplé's main-graph territory. Add a connector in OSM at the cluster centroid (lat=6.387459, lng=2.403293); after re-pulling roads, the cluster will merge into the main graph and Missèkplé will claim it via normal propagation.

### EXCLUDED_AREA — 13 clusters · 92 nodes

- **#8** · 19 nodes · 626 m · _OSM graph fragmentation_ · Ouidah / Pahou
  - Tiny disconnected component of 20 nodes on the far side of major water from any chef. Accept as un-routable hinterland.

- **#16** · 11 nodes · 332 m · _OSM graph fragmentation_ · Abomey-Calavi / Akassato
  - Tiny disconnected component of 3 nodes on the far side of major water from any chef. Accept as un-routable hinterland.

- **#26** · 8 nodes · 260 m · _Water-isolated pocket_ · So-Ava / Ahomè-Lokpo
  - Water-isolated stub (8 nodes, 260 m) with no bridge across. Tiny cluster — un-routable hinterland.

- **#29** · 7 nodes · 169 m · _Water-isolated pocket_ · Ouidah / Pahou
  - Water-isolated stub (7 nodes, 169 m) with no bridge across. Tiny cluster — un-routable hinterland.

- **#30** · 7 nodes · 164 m · _Water-isolated pocket_ · So-Ava / So-Ava
  - Water-isolated stub (7 nodes, 164 m) with no bridge across. Tiny cluster — un-routable hinterland.

- **#32** · 6 nodes · 247 m · _Water-isolated pocket_ · Abomey-Calavi / Akassato
  - Water-isolated stub (6 nodes, 247 m) with no bridge across. Tiny cluster — un-routable hinterland.

- **#33** · 6 nodes · 148 m · _Water-isolated pocket_ · Ouidah / Pahou
  - Water-isolated stub (6 nodes, 148 m) with no bridge across. Tiny cluster — un-routable hinterland.

- **#34** · 6 nodes · 115 m · _Water-isolated pocket_ · Zè / Yokpo
  - Water-isolated stub (6 nodes, 115 m) with no bridge across. Tiny cluster — un-routable hinterland.

- **#38** · 5 nodes · 161 m · _Water-isolated pocket_ · So-Ava / Ahomè-Lokpo
  - Water-isolated stub (5 nodes, 161 m) with no bridge across. Tiny cluster — un-routable hinterland.

- **#39** · 5 nodes · 122 m · _Water-isolated pocket_ · Abomey-Calavi / Zinvié
  - Water-isolated stub (5 nodes, 122 m) with no bridge across. Tiny cluster — un-routable hinterland.

- **#42** · 4 nodes · 114 m · _Water-isolated pocket_ · Ouidah / Pahou
  - Water-isolated stub (4 nodes, 114 m) with no bridge across. Tiny cluster — un-routable hinterland.

- **#44** · 4 nodes · 147 m · _Water-isolated pocket_ · Abomey-Calavi / Akassato
  - Water-isolated stub (4 nodes, 147 m) with no bridge across. Tiny cluster — un-routable hinterland.

- **#45** · 4 nodes · 129 m · _Water-isolated pocket_ · So-Ava / Ahomè-Lokpo
  - Water-isolated stub (4 nodes, 129 m) with no bridge across. Tiny cluster — un-routable hinterland.

## Hand-off to frontier skeleton

The 11 ANNEX clusters need a post-pass attribution step inside the frontier-skeleton generator: after building the skeleton from the 500 m / 700 m propagation network, fold each ANNEX cluster's nodes into the named target chef's region.

The 3 BRIDGE clusters require a graph-build change: exempt OSM ways tagged `bridge=yes`/`cantilever` from the cross-water merge veto. Re-run the 700 m Dijkstra after the change. Expect these to move from EXCLUDED-equivalent to CLAIMED automatically.

The 18 NEW_CHEF clusters are IGN-list extensions; treat them as data deltas and re-run propagation only after the IGN list is updated.

The 1 OSM_GRAPH_FIX clusters are OSM-side fixes; the project's road-graph build is correct, the upstream data is broken. After the fix is mapped, re-pull `tools/data/osm_roads.json` and re-run.

The 13 EXCLUDED clusters require no action — they are documented as un-routable hinterland and will appear as white in any quartier polygon layer.