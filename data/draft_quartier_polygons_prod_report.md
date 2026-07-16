# Draft quartier polygons — production v1 report

## Method

Voronoi tessellation over IGN chef-lieux (Shapely) intersected with per-quartier road-buffer (45 m) and commune polygon. Simplified with Douglas-Peucker (8 m tolerance). Holes < 500 m² filled; polygons < 200 m² dropped.

## Coverage

- polygons produced: **296**
- confidence: HIGH 233 · LOW 63
- by commune:
  - COTONOU: 155
  - ABOMEY-CALAVI: 141

## LOW_CONFIDENCE quartiers (63)

| quartier | commune | area m² | roads m | verts | compactness | reasons |
|---|---|---:|---:|---:|---:|---|
| Agbatô | COTONOU | 26157 | 230 | 8 | 0.628 | few road vertices (8) |
| Gbodjoko | ABOMEY-CALAVI | 530049 | 6251 | 300 | 0.049 | sliver shape (compactness 0.049) |
| Kpaviédja | ABOMEY-CALAVI | 584070 | 11232 | 164 | 0.042 | sliver shape (compactness 0.042) |
| Zèkanmey | ABOMEY-CALAVI | 634282 | 6819 | 348 | 0.039 | sliver shape (compactness 0.039) |
| Golo-Djigbé | ABOMEY-CALAVI | 652509 | 18759 | 946 | 0.037 | sliver shape (compactness 0.037) |
| Golo-Fanto | ABOMEY-CALAVI | 656988 | 11896 | 712 | 0.044 | sliver shape (compactness 0.044) |
| Kpotomey | ABOMEY-CALAVI | 672605 | 8664 | 474 | 0.038 | sliver shape (compactness 0.038) |
| Zinvié-Agolèdji | ABOMEY-CALAVI | 689729 | 7882 | 276 | 0.037 | sliver shape (compactness 0.037) |
| Kpanroun | ABOMEY-CALAVI | 786493 | 10182 | 282 | 0.031 | sliver shape (compactness 0.031) |
| Agonkèssa | ABOMEY-CALAVI | 800570 | 9745 | 524 | 0.039 | sliver shape (compactness 0.039) |
| Yèkon-Do | ABOMEY-CALAVI | 825707 | 10712 | 678 | 0.035 | sliver shape (compactness 0.035) |
| Zinvié-Zounmè | ABOMEY-CALAVI | 829290 | 11712 | 644 | 0.036 | sliver shape (compactness 0.036) |
| Togbin-Daho | ABOMEY-CALAVI | 845357 | 11456 | 578 | 0.048 | sliver shape (compactness 0.048) |
| Adjogansa | ABOMEY-CALAVI | 873761 | 9414 | 550 | 0.030 | sliver shape (compactness 0.030) |
| Azonsa | ABOMEY-CALAVI | 958576 | 12560 | 536 | 0.037 | sliver shape (compactness 0.037) |
| Avagbé | ABOMEY-CALAVI | 1050794 | 20222 | 1060 | 0.024 | sliver shape (compactness 0.024) |
| Zinvié-Fandji | ABOMEY-CALAVI | 1064006 | 15156 | 674 | 0.047 | sliver shape (compactness 0.047) |
| Kolètin | ABOMEY-CALAVI | 1093252 | 13851 | 728 | 0.031 | sliver shape (compactness 0.031) |
| Agonsoudja | ABOMEY-CALAVI | 1105622 | 14163 | 688 | 0.029 | sliver shape (compactness 0.029) |
| Adjamè
 | ABOMEY-CALAVI | 1182845 | 15536 | 502 | 0.024 | sliver shape (compactness 0.024) |
| Kpé | ABOMEY-CALAVI | 1205588 | 14584 | 450 | 0.024 | sliver shape (compactness 0.024) |
| Lohoussa | ABOMEY-CALAVI | 1212634 | 15069 | 770 | 0.029 | sliver shape (compactness 0.029) |
| Sokan | ABOMEY-CALAVI | 1304824 | 18352 | 1006 | 0.025 | sliver shape (compactness 0.025) |
| Dokomè | ABOMEY-CALAVI | 1344216 | 16532 | 826 | 0.026 | sliver shape (compactness 0.026) |
| Togba_Maria-Gléta | ABOMEY-CALAVI | 1348761 | 16844 | 662 | 0.028 | sliver shape (compactness 0.028) |
| Glo-Tokpa | ABOMEY-CALAVI | 1386224 | 18767 | 806 | 0.032 | sliver shape (compactness 0.032) |
| Yèvié | ABOMEY-CALAVI | 1394923 | 16320 | 816 | 0.020 | sliver shape (compactness 0.020) |
| Ahouato | ABOMEY-CALAVI | 1571004 | 18769 | 1058 | 0.026 | sliver shape (compactness 0.026) |
| Zoungo | ABOMEY-CALAVI | 1595702 | 20069 | 1148 | 0.025 | sliver shape (compactness 0.025) |
| Akassato | ABOMEY-CALAVI | 1625920 | 25558 | 1056 | 0.040 | sliver shape (compactness 0.040) |
| Gbétagbo | ABOMEY-CALAVI | 1645436 | 22704 | 1162 | 0.037 | sliver shape (compactness 0.037) |
| Kpodji-Les-Monts | ABOMEY-CALAVI | 1661143 | 21987 | 1006 | 0.019 | sliver shape (compactness 0.019) |
| Alansankomè | ABOMEY-CALAVI | 1732932 | 22431 | 1156 | 0.020 | sliver shape (compactness 0.020) |
| Ahossougbéta | ABOMEY-CALAVI | 1749866 | 26986 | 1034 | 0.050 | sliver shape (compactness 0.050) |
| Ouéga-Agué | ABOMEY-CALAVI | 1780510 | 23983 | 1068 | 0.020 | sliver shape (compactness 0.020) |
| Adjagbo-Aïdjèdo | ABOMEY-CALAVI | 1844984 | 22086 | 980 | 0.022 | sliver shape (compactness 0.022) |
| Domey-Gbo | ABOMEY-CALAVI | 1898346 | 26839 | 1552 | 0.020 | sliver shape (compactness 0.020) |
| Houinmè | ABOMEY-CALAVI | 1911638 | 32017 | 1840 | 0.028 | sliver shape (compactness 0.028) |
| Agonmé | ABOMEY-CALAVI | 1929890 | 25380 | 1374 | 0.024 | sliver shape (compactness 0.024) |
| Ouéga-Tokpa | ABOMEY-CALAVI | 1978420 | 27814 | 1240 | 0.028 | sliver shape (compactness 0.028) |
| Maria-Gléta
 | ABOMEY-CALAVI | 1978670 | 29608 | 1374 | 0.041 | sliver shape (compactness 0.041) |
| Somè | ABOMEY-CALAVI | 2152570 | 33982 | 1280 | 0.028 | sliver shape (compactness 0.028) |
| Togbin-Fandji | ABOMEY-CALAVI | 2153815 | 63840 | 1994 | 0.033 | sliver shape (compactness 0.033) |
| Agongbé | ABOMEY-CALAVI | 2164614 | 24495 | 1180 | 0.012 | sliver shape (compactness 0.012) |
| Ouèdo | ABOMEY-CALAVI | 2324966 | 29421 | 1704 | 0.020 | sliver shape (compactness 0.020) |
| Aïfa-Calavi | ABOMEY-CALAVI | 2339990 | 34934 | 1252 | 0.032 | sliver shape (compactness 0.032) |
| Agassa-Godomey | ABOMEY-CALAVI | 2343023 | 32171 | 1474 | 0.028 | sliver shape (compactness 0.028) |
| Dossounou | ABOMEY-CALAVI | 2347459 | 32899 | 1642 | 0.014 | sliver shape (compactness 0.014) |
| Houinmè-Daho | ABOMEY-CALAVI | 2417432 | 29826 | 1556 | 0.023 | sliver shape (compactness 0.023) |
| Cité-les-Palmiers
 | ABOMEY-CALAVI | 2498322 | 36836 | 1432 | 0.048 | sliver shape (compactness 0.048) |
| Zèkanmey-Domè | ABOMEY-CALAVI | 2558404 | 37199 | 1984 | 0.020 | sliver shape (compactness 0.020) |
| Dessato
 | ABOMEY-CALAVI | 2581595 | 32942 | 1652 | 0.020 | sliver shape (compactness 0.020) |
| Hounzévié
 | ABOMEY-CALAVI | 2831207 | 38312 | 1854 | 0.022 | sliver shape (compactness 0.022) |
| Dassèkomey | ABOMEY-CALAVI | 2875748 | 42678 | 1958 | 0.009 | sliver shape (compactness 0.009) |
| Kansounkpa | ABOMEY-CALAVI | 2944620 | 45956 | 2558 | 0.013 | sliver shape (compactness 0.013) |
| Adovié | ABOMEY-CALAVI | 3002889 | 45897 | 2646 | 0.030 | sliver shape (compactness 0.030) |
| Zoundja
 | ABOMEY-CALAVI | 3093923 | 43575 | 1386 | 0.023 | sliver shape (compactness 0.023) |
| Kpossidja | ABOMEY-CALAVI | 3130728 | 38268 | 1708 | 0.010 | sliver shape (compactness 0.010) |
| Drabo | ABOMEY-CALAVI | 3150401 | 36840 | 1864 | 0.010 | sliver shape (compactness 0.010) |
| Djèkpota | ABOMEY-CALAVI | 3195115 | 78598 | 3572 | 0.019 | sliver shape (compactness 0.019) |
| Akossavié | ABOMEY-CALAVI | 3270508 | 45068 | 2544 | 0.033 | sliver shape (compactness 0.033) |
| Hêvié | ABOMEY-CALAVI | 3416526 | 43702 | 2390 | 0.014 | sliver shape (compactness 0.014) |
| Cococodji | ABOMEY-CALAVI | 5037697 | 170259 | 5968 | 0.020 | sliver shape (compactness 0.020) |
