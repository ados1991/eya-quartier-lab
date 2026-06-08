# OSM amenity → quartier audit

_Source_: `osm_amenities.json` (ODbL, derivative datasets allowed)

## Signal quality

| Metric | Value | Target |
|---|---:|---|
| POIs total | 2353 | — |
| Matched a quartier name | 189 (8.0 %) | ≥ 20 % ✗ |
| Disputes detected | 103 | ≥ 5 |

### Match modes

| Mode | Count |
|---|---:|
| FULL_SINGLE_UNIQUE | 118 |
| TOKEN_UNIQUE | 67 |
| FULL_HYPHEN | 4 |

### POI vs current propagation

| Class | Count | % |
|---|---:|---:|
| CONFIRM | 76 | 40.2 % |
| DISPUTE | 103 | 54.5 % |
| FILLS_GAP | 4 | 2.1 % |
| NO_NODE | 6 | 3.2 % |

## Top disputed pairs

| POI says | Propagation says | # |
|---|---|---:|
| Védokô | Missogbé | 3 |
| Togba_Maria-Gléta | Ouéga-Tokpa | 3 |
| Mènontin | Kindonou | 3 |
| Togba_Maria-Gléta | Houèto | 3 |
| Ladji | Ahouansori-Towéta-Kpota | 3 |
| Gbéto | Sèdjro-Saint-Michel | 2 |
| Gbéto | Dota | 2 |
| Agori | Fifonsi
 | 2 |
| Akpakpa-Dodomè | Lom-Nava | 2 |
| Cité-la-Victoire
 | Aïtchédji
 | 2 |
| Houèto | Tankpê-Yoho | 2 |
| Agbatô | Hlacômey | 2 |
| Gbétagbo | Agassa-Godomey | 2 |
| Védokô | Sètôvi | 2 |
| Tokplégbé | Dandji-Hokanmè | 2 |
| Cocotomey | Tokpa
 | 2 |
| Sèdjro-Saint-Michel | Djoukpa-Togoudo
 | 1 |
| Sèdjro-Saint-Michel | Mifongou | 1 |
| Zogbo | Agounvocôdji | 1 |
| Cocotomey | Fandji
 | 1 |
| Haie-Vive-Cocotiers | Cadjèhoun-Agonga | 1 |
| Midombo | Kpankpan | 1 |
| Agla-Petit-Château | Todoté | 1 |
| Agontinkon | Vodjè-Ayidoté | 1 |
| Espace-Saint | Ounvènoumèdé
 | 1 |
| Agla-Les-Pylônes | Agla-Petit-Château | 1 |
| Cité-la-Victoire
 | Agori | 1 |
| Sèdjro-Saint-Michel | Agamandin | 1 |
| Tokan | Ahossougbéta | 1 |
| Akpakpa-Dodomè | Nvènamèdé | 1 |

## Verdict

**Weak signal.** Hit rate 8.0 %. Review unmatched sample to refine stopwords, or accept that POI labels aren't a strong source for this metro.

## 30 unmatched POI names (sample, for stopword tuning)

- `Complexe Scolaire Godomey Houalakomey A-B-C`
- `ACFB`
- `Sêzo`
- `Sonacop`
- `Hôtel Peace and Love`
- `Domino`
- `CSP de Godomey`
- `Le Lambi's`
- `Mairie du 10ᵉ arrondissement`
- `El Dorado Beach Club`
- `Collège d'Enseignement Général l'Océan`
- `Bénin Petro`
- `Banque Internationale d'industrie et de Commerce`
- `Le Macumba`
- `Église de Jésus Christ des Saints des Derniers jours`
- `BANK OF AFRICA`
- `Hôtel du lac`
- `Maison des Jeunes de Godomey`
- `Chant d'oiseau`
- `Bank of Africa`
- `Ramatuelle`
- `BGFI Bank`
- `BP`
- `Chez Papa Poochy`
- `Centre Nutironnel Jean Pliya`
- `MRS`
- `Cyber Notre Dame`
- `Ministère de la Nontagne de Feu et des Miracles (MFM) Godomey`
- `Atlantic Banque, Agence Ganhi`
- `Pharmacie Sainte Cecile`