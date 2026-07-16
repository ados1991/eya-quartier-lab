# Draft quartier polygons — v2 (road-ownership-derived)

## Method

Polygons are the geometric envelope of the validated road ownership.
Chef-lieu Voronoi was NOT used.

Pipeline: class-aware road buffers per quartier (motorway/trunk/primary 30 m, secondary/tertiary 22 m, residential/unclassified 18 m, service/track 12 m) → union per quartier → rasterize the commune area at 30 m grid → for each cell inside the coverage envelope + inside a commune, assign the OWNER of the NEAREST OWNED ROAD VERTEX (KDTree over ~72 000 owned road vertices) → extract per-owner polygon via row-strip union → Douglas-Peucker simplify (8 m) → fill holes < 500 m² → drop slivers < 200 m² → clip to owning commune.

If you hide the polygons and display only the coloured roads, the polygon boundary follows those roads naturally.

## Coverage

- polygons produced: **298**
- confidence: HIGH 139 · LOW 159
- COTONOU: 156
- ABOMEY-CALAVI: 142

## LOW confidence quartiers

| quartier | commune | area m² | roads m | verts | compactness | reasons |
|---|---|---:|---:|---:|---:|---|
| Agbatô | COTONOU | 18900 | 230 | 8 | 0.125 | few road vertices (8) |
| Espace-Saint | ABOMEY-CALAVI | 124010 | 3218 | 234 | 0.019 | thread-shaped (compactness 0.019) |
| Gbénonkpô | COTONOU | 144000 | 3817 | 82 | 0.019 | thread-shaped (compactness 0.019) |
| Houégoudo
 | ABOMEY-CALAVI | 178748 | 5671 | 336 | 0.016 | thread-shaped (compactness 0.016) |
| Djigbo | ABOMEY-CALAVI | 185395 | 8693 | 324 | 0.017 | thread-shaped (compactness 0.017) |
| Hadjanaho | ABOMEY-CALAVI | 185400 | 5457 | 172 | 0.011 | thread-shaped (compactness 0.011) |
| Missogbé | COTONOU | 186300 | 4854 | 164 | 0.018 | thread-shaped (compactness 0.018) |
| Hêdomè
 | ABOMEY-CALAVI | 189900 | 5004 | 188 | 0.019 | thread-shaped (compactness 0.019) |
| Tonato | COTONOU | 201600 | 5484 | 146 | 0.019 | thread-shaped (compactness 0.019) |
| Anagbo | ABOMEY-CALAVI | 208118 | 13711 | 394 | 0.013 | thread-shaped (compactness 0.013) |
| Missèkplé | COTONOU | 208800 | 5816 | 110 | 0.013 | thread-shaped (compactness 0.013) |
| Cadjèhoun-Kpota | COTONOU | 215100 | 6322 | 174 | 0.014 | thread-shaped (compactness 0.014) |
| Védokô | COTONOU | 223200 | 6160 | 184 | 0.019 | thread-shaped (compactness 0.019) |
| Djoukpa-Togoudo
 | ABOMEY-CALAVI | 226800 | 6043 | 252 | 0.018 | thread-shaped (compactness 0.018) |
| Zogbo | COTONOU | 235800 | 6711 | 222 | 0.018 | thread-shaped (compactness 0.018) |
| Fignonhou
 | ABOMEY-CALAVI | 238500 | 6655 | 222 | 0.014 | thread-shaped (compactness 0.014) |
| Kpaviédja | ABOMEY-CALAVI | 242167 | 11232 | 164 | 0.011 | thread-shaped (compactness 0.011) |
| Aïbatin-Dodo | COTONOU | 243000 | 6678 | 194 | 0.017 | thread-shaped (compactness 0.017) |
| Abikouholi
 | ABOMEY-CALAVI | 245700 | 7023 | 196 | 0.014 | thread-shaped (compactness 0.014) |
| Gbodjoko | ABOMEY-CALAVI | 247120 | 6251 | 300 | 0.012 | thread-shaped (compactness 0.012) |
| Agla-Centre | COTONOU | 248822 | 7141 | 222 | 0.017 | thread-shaped (compactness 0.017) |
| Gninkindji
 | ABOMEY-CALAVI | 252900 | 7054 | 266 | 0.019 | thread-shaped (compactness 0.019) |
| Yèvié-Nougo | ABOMEY-CALAVI | 254700 | 6503 | 326 | 0.012 | thread-shaped (compactness 0.012) |
| Agla-Petit-Château | COTONOU | 260100 | 7124 | 246 | 0.019 | thread-shaped (compactness 0.019) |
| Agounvocôdji | COTONOU | 262800 | 6972 | 244 | 0.014 | thread-shaped (compactness 0.014) |
| Tokpa-Zoungo-Sud
 | ABOMEY-CALAVI | 266400 | 8607 | 358 | 0.018 | thread-shaped (compactness 0.018) |
| Agla-Les-Pylônes | COTONOU | 268123 | 12131 | 452 | 0.018 | thread-shaped (compactness 0.018) |
| Yêkon-Aga | ABOMEY-CALAVI | 269100 | 6453 | 348 | 0.013 | thread-shaped (compactness 0.013) |
| Zèkanmey | ABOMEY-CALAVI | 270900 | 6819 | 348 | 0.010 | thread-shaped (compactness 0.010) |
| Fifadji-Houto (Jak) | COTONOU | 278100 | 8203 | 200 | 0.014 | thread-shaped (compactness 0.014) |
| Gbèdiga-Guêdêhounguè | COTONOU | 279000 | 7518 | 222 | 0.017 | thread-shaped (compactness 0.017) |
| Dandji-Hokanmè | COTONOU | 279527 | 23966 | 760 | 0.016 | thread-shaped (compactness 0.016) |
| Ningboto
 | ABOMEY-CALAVI | 283500 | 8091 | 218 | 0.012 | thread-shaped (compactness 0.012) |
| Avotrou-Aïmonlonfidé | COTONOU | 290700 | 7898 | 226 | 0.017 | thread-shaped (compactness 0.017) |
| Gbèdjromèdè-Nord | COTONOU | 294300 | 8123 | 156 | 0.012 | thread-shaped (compactness 0.012) |
| Énagnon | COTONOU | 294300 | 8682 | 266 | 0.013 | thread-shaped (compactness 0.013) |
| Golo-Fanto | ABOMEY-CALAVI | 294701 | 11896 | 712 | 0.009 | thread-shaped (compactness 0.009) |
| Sèdomey | ABOMEY-CALAVI | 295200 | 8076 | 284 | 0.013 | thread-shaped (compactness 0.013) |
| Tchanhounkpamè | COTONOU | 296061 | 22961 | 724 | 0.017 | thread-shaped (compactness 0.017) |
| Zounga
 | ABOMEY-CALAVI | 296100 | 8172 | 250 | 0.017 | thread-shaped (compactness 0.017) |
| Finagnon | COTONOU | 299700 | 8767 | 230 | 0.013 | thread-shaped (compactness 0.013) |
| Zinvié-Agolèdji | ABOMEY-CALAVI | 301216 | 7882 | 276 | 0.011 | thread-shaped (compactness 0.011) |
| Kouhounou | COTONOU | 327600 | 8800 | 336 | 0.016 | thread-shaped (compactness 0.016) |
| Zongo-Ehuzu | COTONOU | 333900 | 8293 | 240 | 0.013 | thread-shaped (compactness 0.013) |
| Fidjrossè-Centre | COTONOU | 342000 | 8993 | 296 | 0.013 | thread-shaped (compactness 0.013) |
| Houéyihô-Tannou | COTONOU | 349200 | 8980 | 374 | 0.014 | thread-shaped (compactness 0.014) |
| Kpotomey | ABOMEY-CALAVI | 352800 | 8664 | 474 | 0.009 | thread-shaped (compactness 0.009) |
| Agonkanmey
 | ABOMEY-CALAVI | 352800 | 10028 | 408 | 0.010 | thread-shaped (compactness 0.010) |
| Fifadji | COTONOU | 361800 | 9932 | 292 | 0.011 | thread-shaped (compactness 0.011) |
| Cité-la-Victoire
 | ABOMEY-CALAVI | 373500 | 10328 | 404 | 0.009 | thread-shaped (compactness 0.009) |
| Kpanroun | ABOMEY-CALAVI | 382500 | 10182 | 282 | 0.007 | thread-shaped (compactness 0.007) |
| Agonkèssa | ABOMEY-CALAVI | 385200 | 9745 | 524 | 0.009 | thread-shaped (compactness 0.009) |
| Logbozounkpa | ABOMEY-CALAVI | 385200 | 10441 | 344 | 0.012 | thread-shaped (compactness 0.012) |
| Zogbohouè | COTONOU | 388800 | 10569 | 362 | 0.013 | thread-shaped (compactness 0.013) |
| Adjogansa | ABOMEY-CALAVI | 388800 | 9414 | 550 | 0.007 | thread-shaped (compactness 0.007) |
| Dèkoungbé
 | ABOMEY-CALAVI | 389700 | 10701 | 332 | 0.009 | thread-shaped (compactness 0.009) |
| Agbo Codji Sèdégbé | ABOMEY-CALAVI | 396000 | 10966 | 408 | 0.013 | thread-shaped (compactness 0.013) |
| Togbin-Kpèvi | ABOMEY-CALAVI | 406800 | 11090 | 430 | 0.010 | thread-shaped (compactness 0.010) |
| Hounsa-Agbodokpa
 | ABOMEY-CALAVI | 415800 | 10813 | 376 | 0.010 | thread-shaped (compactness 0.010) |
| Yèkon-Do | ABOMEY-CALAVI | 421200 | 10712 | 678 | 0.007 | thread-shaped (compactness 0.007) |
| Gbodjo | ABOMEY-CALAVI | 421200 | 11396 | 424 | 0.010 | thread-shaped (compactness 0.010) |
| Togbin-Daho | ABOMEY-CALAVI | 422100 | 11456 | 578 | 0.009 | thread-shaped (compactness 0.009) |
| Gbègnigan-Midokpo
 | ABOMEY-CALAVI | 424800 | 11360 | 424 | 0.011 | thread-shaped (compactness 0.011) |
| Zinvié-Zounmè | ABOMEY-CALAVI | 432900 | 11712 | 644 | 0.007 | thread-shaped (compactness 0.007) |
| Tokpa-Zoungo-Nord
 | ABOMEY-CALAVI | 445500 | 12136 | 406 | 0.009 | thread-shaped (compactness 0.009) |
| Adjaha-Cité | COTONOU | 461700 | 12784 | 394 | 0.010 | thread-shaped (compactness 0.010) |
| Assrossa
 | ABOMEY-CALAVI | 475200 | 13190 | 500 | 0.007 | thread-shaped (compactness 0.007) |
| Fiyégnon-Jacquot | COTONOU | 480317 | 15821 | 510 | 0.008 | thread-shaped (compactness 0.008) |
| Azonsa | ABOMEY-CALAVI | 493200 | 12560 | 536 | 0.008 | thread-shaped (compactness 0.008) |
| Cocotomey | ABOMEY-CALAVI | 494100 | 13168 | 412 | 0.010 | thread-shaped (compactness 0.010) |
| Ahouanlèko | COTONOU | 501082 | 21385 | 618 | 0.009 | thread-shaped (compactness 0.009) |
| Mènontin | COTONOU | 504000 | 13481 | 430 | 0.008 | thread-shaped (compactness 0.008) |
| Yénandjro
 | ABOMEY-CALAVI | 504900 | 13730 | 604 | 0.008 | thread-shaped (compactness 0.008) |
| Kpé | ABOMEY-CALAVI | 517500 | 14584 | 450 | 0.006 | thread-shaped (compactness 0.006) |
| Agonsoudja | ABOMEY-CALAVI | 530100 | 14163 | 688 | 0.005 | thread-shaped (compactness 0.005) |
| Plateau
 | ABOMEY-CALAVI | 537300 | 14576 | 492 | 0.009 | thread-shaped (compactness 0.009) |
| Tokpa
 | ABOMEY-CALAVI | 537300 | 15212 | 548 | 0.010 | thread-shaped (compactness 0.010) |
| Kolètin | ABOMEY-CALAVI | 551700 | 13851 | 728 | 0.006 | thread-shaped (compactness 0.006) |
| Dénou
 | ABOMEY-CALAVI | 560700 | 15072 | 528 | 0.010 | thread-shaped (compactness 0.010) |
| Tankpè-Togoudo | ABOMEY-CALAVI | 571500 | 15209 | 736 | 0.009 | thread-shaped (compactness 0.009) |
| Agamandin | ABOMEY-CALAVI | 579600 | 15845 | 642 | 0.007 | thread-shaped (compactness 0.007) |
| Lohoussa | ABOMEY-CALAVI | 580500 | 15069 | 770 | 0.005 | thread-shaped (compactness 0.005) |
| Zinvié-Fandji | ABOMEY-CALAVI | 581400 | 15156 | 674 | 0.007 | thread-shaped (compactness 0.007) |
| Adjamè
 | ABOMEY-CALAVI | 583826 | 15536 | 502 | 0.005 | thread-shaped (compactness 0.005) |
| La-Paix
 | ABOMEY-CALAVI | 596700 | 16634 | 600 | 0.011 | thread-shaped (compactness 0.011) |
| Houèkè-Gbo | ABOMEY-CALAVI | 620100 | 16085 | 682 | 0.007 | thread-shaped (compactness 0.007) |
| Sèmè | ABOMEY-CALAVI | 625500 | 17105 | 608 | 0.007 | thread-shaped (compactness 0.007) |
| Yèvié | ABOMEY-CALAVI | 630000 | 16320 | 816 | 0.004 | thread-shaped (compactness 0.004) |
| Finafa
 | ABOMEY-CALAVI | 637200 | 16833 | 640 | 0.007 | thread-shaped (compactness 0.007) |
| Togba_Maria-Gléta | ABOMEY-CALAVI | 645300 | 16844 | 662 | 0.006 | thread-shaped (compactness 0.006) |
| Dokomè | ABOMEY-CALAVI | 653400 | 16532 | 826 | 0.005 | thread-shaped (compactness 0.005) |
| Golo-Djigbé | ABOMEY-CALAVI | 658116 | 18759 | 946 | 0.005 | thread-shaped (compactness 0.005) |
| Zogbadjè | ABOMEY-CALAVI | 659700 | 19821 | 642 | 0.005 | thread-shaped (compactness 0.005) |
| Agori | ABOMEY-CALAVI | 668700 | 17087 | 748 | 0.007 | thread-shaped (compactness 0.007) |
| Tankpê-Yoho | ABOMEY-CALAVI | 669600 | 18333 | 896 | 0.007 | thread-shaped (compactness 0.007) |
| Gbodjè-Womey
 | ABOMEY-CALAVI | 684900 | 19442 | 626 | 0.008 | thread-shaped (compactness 0.008) |
| Alédjo
 | ABOMEY-CALAVI | 710100 | 19206 | 664 | 0.007 | thread-shaped (compactness 0.007) |
| Amahoun
 | ABOMEY-CALAVI | 723600 | 19914 | 700 | 0.006 | thread-shaped (compactness 0.006) |
| Ounvènoumèdé
 | ABOMEY-CALAVI | 725400 | 19578 | 722 | 0.006 | thread-shaped (compactness 0.006) |
| Glo-Tokpa | ABOMEY-CALAVI | 732600 | 18767 | 806 | 0.005 | thread-shaped (compactness 0.005) |
| Zopah-Akassato | ABOMEY-CALAVI | 734400 | 20501 | 488 | 0.005 | thread-shaped (compactness 0.005) |
| Tchinangbégbo
 | ABOMEY-CALAVI | 735300 | 19277 | 628 | 0.006 | thread-shaped (compactness 0.006) |
| Avagbé | ABOMEY-CALAVI | 740700 | 20222 | 1060 | 0.004 | thread-shaped (compactness 0.004) |
| Sokan | ABOMEY-CALAVI | 750600 | 18352 | 1006 | 0.004 | thread-shaped (compactness 0.004) |
| Alègléta | ABOMEY-CALAVI | 752400 | 19694 | 864 | 0.005 | thread-shaped (compactness 0.005) |
| Tokan | ABOMEY-CALAVI | 754200 | 20831 | 894 | 0.005 | thread-shaped (compactness 0.005) |
| Ahouato | ABOMEY-CALAVI | 757800 | 18769 | 1058 | 0.005 | thread-shaped (compactness 0.005) |
| Atrokpo-Codji | ABOMEY-CALAVI | 803700 | 22914 | 730 | 0.005 | thread-shaped (compactness 0.005) |
| Kpodji-Les-Monts | ABOMEY-CALAVI | 828900 | 21987 | 1006 | 0.004 | thread-shaped (compactness 0.004) |
| Aïdégnon
 | ABOMEY-CALAVI | 829800 | 22182 | 910 | 0.006 | thread-shaped (compactness 0.006) |
| Zoungo | ABOMEY-CALAVI | 831600 | 20069 | 1148 | 0.004 | thread-shaped (compactness 0.004) |
| Adjagbo-Aïdjèdo | ABOMEY-CALAVI | 851400 | 22086 | 980 | 0.004 | thread-shaped (compactness 0.004) |
| Misséssinto | ABOMEY-CALAVI | 866700 | 22127 | 1142 | 0.005 | thread-shaped (compactness 0.005) |
| Fandji
 | ABOMEY-CALAVI | 867600 | 25070 | 728 | 0.005 | thread-shaped (compactness 0.005) |
| Alansankomè | ABOMEY-CALAVI | 872100 | 22431 | 1156 | 0.004 | thread-shaped (compactness 0.004) |
| Fifonsi
 | ABOMEY-CALAVI | 884700 | 24602 | 934 | 0.005 | thread-shaped (compactness 0.005) |
| Gbétagbo | ABOMEY-CALAVI | 888300 | 22704 | 1162 | 0.005 | thread-shaped (compactness 0.005) |
| Womey-Yénawa | ABOMEY-CALAVI | 905400 | 23196 | 1148 | 0.004 | thread-shaped (compactness 0.004) |
| Haie-Vive-Cocotiers | COTONOU | 908100 | 24756 | 898 | 0.006 | thread-shaped (compactness 0.006) |
| Sogan | ABOMEY-CALAVI | 915300 | 23674 | 1226 | 0.005 | thread-shaped (compactness 0.005) |
| Sodo
 | ABOMEY-CALAVI | 919800 | 24518 | 978 | 0.005 | thread-shaped (compactness 0.005) |
| Adjagbo | ABOMEY-CALAVI | 925200 | 21777 | 1262 | 0.003 | thread-shaped (compactness 0.003) |
| Ouéga-Agué | ABOMEY-CALAVI | 928800 | 23983 | 1068 | 0.003 | thread-shaped (compactness 0.003) |
| Agongbé | ABOMEY-CALAVI | 951300 | 24495 | 1180 | 0.003 | thread-shaped (compactness 0.003) |
| Houèto | ABOMEY-CALAVI | 954000 | 25784 | 1074 | 0.004 | thread-shaped (compactness 0.004) |
| Womey-Centre
 | ABOMEY-CALAVI | 965700 | 25190 | 1286 | 0.005 | thread-shaped (compactness 0.005) |
| Aïtchédji
 | ABOMEY-CALAVI | 972000 | 25557 | 822 | 0.005 | thread-shaped (compactness 0.005) |
| Agonmé | ABOMEY-CALAVI | 983700 | 25380 | 1374 | 0.003 | thread-shaped (compactness 0.003) |
| Houinmè | ABOMEY-CALAVI | 1002660 | 32017 | 1840 | 0.003 | thread-shaped (compactness 0.003) |
| Zopah-Kokpo | ABOMEY-CALAVI | 1008000 | 28438 | 846 | 0.005 | thread-shaped (compactness 0.005) |
| Houèkè-Honou | ABOMEY-CALAVI | 1050300 | 29301 | 758 | 0.004 | thread-shaped (compactness 0.004) |
| Ahossougbéta | ABOMEY-CALAVI | 1055700 | 26986 | 1034 | 0.004 | thread-shaped (compactness 0.004) |
| Ouéga-Tokpa | ABOMEY-CALAVI | 1069200 | 27814 | 1240 | 0.003 | thread-shaped (compactness 0.003) |
| Domey-Gbo | ABOMEY-CALAVI | 1069200 | 26839 | 1552 | 0.003 | thread-shaped (compactness 0.003) |
| Tankpè-Tanmè | ABOMEY-CALAVI | 1071000 | 27950 | 1218 | 0.004 | thread-shaped (compactness 0.004) |
| Akassato | ABOMEY-CALAVI | 1078200 | 25558 | 1056 | 0.004 | thread-shaped (compactness 0.004) |
| Godomey-N'Gbèho | ABOMEY-CALAVI | 1118700 | 30890 | 954 | 0.004 | thread-shaped (compactness 0.004) |
| Maria-Gléta
 | ABOMEY-CALAVI | 1126800 | 29608 | 1374 | 0.004 | thread-shaped (compactness 0.004) |
| Dossounou | ABOMEY-CALAVI | 1171275 | 32899 | 1642 | 0.003 | thread-shaped (compactness 0.003) |
| Houinmè-Daho | ABOMEY-CALAVI | 1178100 | 29826 | 1556 | 0.003 | thread-shaped (compactness 0.003) |
| Ouèdo | ABOMEY-CALAVI | 1207800 | 29421 | 1704 | 0.003 | thread-shaped (compactness 0.003) |
| Agassa-Godomey | ABOMEY-CALAVI | 1253700 | 32171 | 1474 | 0.003 | thread-shaped (compactness 0.003) |
| Dessato
 | ABOMEY-CALAVI | 1268100 | 32942 | 1652 | 0.003 | thread-shaped (compactness 0.003) |
| Dassèkomey | ABOMEY-CALAVI | 1278416 | 42678 | 1958 | 0.002 | thread-shaped (compactness 0.002) |
| Aïfa-Calavi | ABOMEY-CALAVI | 1298700 | 34934 | 1252 | 0.003 | thread-shaped (compactness 0.003) |
| Somè | ABOMEY-CALAVI | 1320300 | 33982 | 1280 | 0.003 | thread-shaped (compactness 0.003) |
| Cité-les-Palmiers
 | ABOMEY-CALAVI | 1369800 | 36836 | 1432 | 0.003 | thread-shaped (compactness 0.003) |
| Hounzévié
 | ABOMEY-CALAVI | 1429448 | 38312 | 1854 | 0.003 | thread-shaped (compactness 0.003) |
| Drabo | ABOMEY-CALAVI | 1434600 | 36840 | 1864 | 0.002 | thread-shaped (compactness 0.002) |
| Zèkanmey-Domè | ABOMEY-CALAVI | 1471500 | 37199 | 1984 | 0.002 | thread-shaped (compactness 0.002) |
| Kpossidja | ABOMEY-CALAVI | 1515600 | 38268 | 1708 | 0.002 | thread-shaped (compactness 0.002) |
| Zoundja
 | ABOMEY-CALAVI | 1549800 | 43575 | 1386 | 0.002 | thread-shaped (compactness 0.002) |
| Hêvié | ABOMEY-CALAVI | 1619021 | 43702 | 2390 | 0.002 | thread-shaped (compactness 0.002) |
| Akossavié | ABOMEY-CALAVI | 1787400 | 45068 | 2544 | 0.002 | thread-shaped (compactness 0.002) |
| Kansounkpa | ABOMEY-CALAVI | 1798200 | 45956 | 2558 | 0.002 | thread-shaped (compactness 0.002) |
| Adovié | ABOMEY-CALAVI | 1815300 | 45897 | 2646 | 0.002 | thread-shaped (compactness 0.002) |
| Djèkpota | ABOMEY-CALAVI | 2225735 | 78598 | 3572 | 0.002 | thread-shaped (compactness 0.002) |
| Togbin-Fandji | ABOMEY-CALAVI | 2275200 | 63840 | 1994 | 0.002 | thread-shaped (compactness 0.002) |
| Cococodji | ABOMEY-CALAVI | 5305611 | 170259 | 5968 | 0.001 | thread-shaped (compactness 0.001) |
