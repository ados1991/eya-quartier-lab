# EYA — Quartier polygon evaluation lab

**Status:** EXPERIMENTAL. Drafts only. NOT validated. NOT for app detection.

This is a public-shareable evaluation lab for draft quartier polygons of
**Cotonou + Abomey-Calavi (Bénin)**. Three generation strategies are shown
side-by-side so the polygons can be reviewed, criticised, and compared.

Open `index.html` to inspect the interactive map.

## What you're looking at

We're trying to produce a usable boundary for each of the ~310 quartiers
that make up Cotonou + Abomey-Calavi, for delivery-app purposes. **No open
dataset of authoritative Bénin quartier polygons exists** — we checked
exhaustively. So we generate drafts from every available signal and
compare versions.

### Three versions, same dataset

| Version | Algorithm | Confidence colors |
|---------|-----------|-------------------|
| **v1 — pure Voronoi** | Nearest-seed partition from IGN chef-lieu points. No clipping. Regression baseline only. | grey |
| **v2 — Voronoi + arr-clip** | Same as v1, then intersected with the IGN arrondissement polygon (Cotonou 13, Abomey-Calavi 9). Previous default. | green/orange/red by anchor count |
| **v3 — topology-aware** | Multi-source Dijkstra on a 100 m raster grid. **Water cells (canals/lagoon) are forbidden**, **road cells are cheap (0.3 cost)**, **POIs whose name contains the quartier name act as additional seeds**. Each cell ends up owned by the quartier with lowest cost-distance. | teal |
| **v4 — asymmetric water-barrier (experimental)** | v3 + per-quartier "home land component(s)". Stepping into a non-home connected component costs +8. Bridges (incl. Pont MLK) reconnect. POI evidence in another component extends the home set. Works where water actually disconnects (AC lake fingers); does very little inside Cotonou where bridges keep all land in one component. | purple |
| **v5 — canal-side asymmetric barrier (experimental)** | v3 + per-quartier "home side" of each nearby canal/river/stream (>200 m). Inside the 500 m buffer of a waterway, stepping from the chef-lieu's side into the opposite side costs +25 per crossing. POI evidence on the other bank flips that waterway to "both" (no penalty). Generic — not hardcoded to any pair of quartiers. | orange |

The conceptual move from v2 to v3: **stop generating polygons directly,
generate territorial influence fields, then derive polygons from those.**

### Disputed strips (v3 only)

Cells where the cost-gap to the second-best owner is small are marked as
**disputed strips** — the fuzzy boundary zones where two quartiers
compete for territory. Shown in red. 485 such strips in the v3 output.

## Data sources

- **IGN-Bénin** chef-lieu register (`ign_points.geojson`) — primary
  official centroid source. Filtered to Cotonou + Abomey-Calavi.
  Source: <https://ign.bj/webmap/assets/layer/data_chef_lieu_village.geojson>
- **IGN-Bénin** arrondissement boundaries (`arrondissement_polygons.geojson`)
  — outer clip per quartier. Source: <https://ign.bj/webmap/assets/layer/limite_arrondissement.geojson>
- **OpenStreetMap** roads + waterways — the topological cost grid for v3.
- **OpenStreetMap** amenities (`poi_index.geojson`) — churches, police,
  fuel, hospitals, schools, banks, markets, hotels (2 662 entries with
  categories + names).
- **Mapbox** geocoding — independent locality confirmation (40 places).
- **Google** geocoding — supporting signal (subject to ToS).
- ~~**cadastre.bj**~~ — **EVALUATED AND REJECTED**. Its polygons
  conflict with IGN/local reality in key areas (e.g. it labels IGN's
  Midédji centre as Yenawa). Not used for any decision here.

## Known limitations

- **No source agrees with another** in disputed zones (Midedji /
  Zogbo / Sainte-Rita / Zezoumè). This isn't a bug in our pipeline —
  Bénin quartier boundaries are officially *"poorly identified / a source
  of land disputes"*. No single source is ground truth.
- **v3's Dijkstra still uses cost-distance, not perfect topology.**
  Bridges across canals aren't modelled — territory cannot cross water
  even where a bridge exists in reality.
- **Colloquial supra-quartier names** (Sainte-Rita, Akpakpa, Zezoumè
  in some areas) don't exist as IGN quartiers, so they get no polygon.
  Their named POIs pull territory toward the IGN quartier they sit
  inside, which can be misleading.
- **39 quartiers couldn't be IGN-matched** (name-spelling variants like
  our `HPUEYIHO` → IGN's `Houéyiho`) and produce no draft.
- v3 polygon edges are crenellated because cells are 100 m squares.
  Smoothing is intentionally minimal.

## How to inspect issues

1. Open `index.html` — toggle v1/v2/v3 on/off to see how each version
   handles the same area.
2. Toggle `v3 disputed strips` to see the transition zones.
3. Click any polygon → popup with version, confidence, evidence (cell
   count, POI seeds, mean cost-gap).
4. Compare polygons against:
   - IGN chef-lieu points (turquoise dots with permanent name labels).
   - Arrondissement shells (navy dashed).
   - OSM amenities (emoji pins with names; toggle on).
5. Screenshots of known problem areas are in `screenshots/`.

## Files in `data/`

| File | What |
|------|------|
| `draft_quartier_polygons_v1.geojson` | v1 polygons (pure Voronoi) |
| `draft_quartier_polygons_v2.geojson` | v2 polygons (Voronoi + arr-clipped) |
| `draft_quartier_polygons_v3.geojson` | v3 polygons (topology-aware) |
| `draft_quartier_disputed_v3.geojson` | v3 transition strips |
| `draft_quartier_evidence_v3.json` | v3 per-quartier diagnostics |
| `ign_points.geojson` | IGN chef-lieu points for Cotonou + AC |
| `arrondissement_polygons.geojson` | IGN arrondissement boundaries |
| `poi_index.geojson` | OSM amenities (category + name) |

## Notes for AI-assisted review

If you've been asked to review this lab via an AI assistant (ChatGPT,
Claude, etc.):
- The GeoJSON files in `data/` are the source of truth — attach them
  directly to the chat for quantitative analysis.
- Treat all polygons as **draft hypotheses**, not authoritative
  boundaries. Disagreement between v1/v2/v3 is informative, not a bug.
- Cadastre.bj polygons are excluded by the project's product decision.
  Do not re-introduce them as ground truth.
- Specific issues being investigated:
  - The Midedji / Yenawa-Fifadji / Zezoumè / Sainte-Rita corridor
    (10th arrondissement of Cotonou, around lat 6.388, lng 2.393).
  - Whether v3's road-following territory better matches local reality
    than v2's straight Voronoi diagonals.
  - Whether canal-as-barrier behaviour in v3 correctly separates the
    Fifadji channel's two banks.

## Serving locally

The page uses `fetch('data/…')` so it requires HTTP (not `file://`):

```
python -m http.server 8000
# then open http://localhost:8000/index.html
```

For sharing: drop the whole folder onto <https://app.netlify.com/drop>
or push to a GitHub Pages repo.

## Reproducibility

Generated by:
- `tools/build_draft_quartier_polygons.py` → v1 + v2.
- `tools/build_draft_v3_topology.py` → v3 + disputed strips.
- `tools/build_public_quartier_lab.py` → this folder.

Internal tracer (with drawing/validation flow, gated by Mapbox token):
`tools/centroids_map.html`. Not included in this public bundle.

— Data © OpenStreetMap contributors (ODbL) · IGN-Bénin · INStaD RGPH
