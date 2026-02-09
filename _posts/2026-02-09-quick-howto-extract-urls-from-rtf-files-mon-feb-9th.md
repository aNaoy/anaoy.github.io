---
title: 'Quick Howto: Extract URLs from RTF files, (Mon, Feb 9th)'
date: 2026-02-09
permalink: /posts/2026/02/09/quick-howto-extract-urls-from-rtf-files-mon-feb-9th/
tags:
- veille-cyber
- sans-isc
---
### Extraction de Liens Malveillants depuis des Documents RTF

L'article décrit une méthode pour identifier des liens potentiellement malveillants contenus dans des fichiers RTF, qui sont souvent utilisés dans des campagnes d'attaques. Ces fichiers peuvent dissimuler des URL en utilisant l'extension .doc, une tactique courante employée par les acteurs malveillants.

**Points Clés :**

*   Des documents RTF sont exploités par des groupes comme APT28 pour diffuser des attaques, notamment via la vulnérabilité CVE-2026-21509.
*   Une série d'outils Python (rtfdump.py, strings.py, re-search.py) est proposée pour analyser le contenu des fichiers RTF et en extraire les URL.
*   L'analyse peut révéler des domaines, des adresses IP privées, des chemins UNC et des URL malformées, potentiellement utilisées pour des requêtes WebDAV.

**Vulnérabilités :**

*   **CVE-2026-21509** : Mentionnée comme étant exploitée par APT28 via des documents RTF.

**Recommandations :**

*   Utiliser la commande `rtfdump.py -j -C SAMPLE.vir | strings.py --jsoninput | re-search.py -n url -u -F officeurls` pour analyser un fichier RTF suspect (remplacer `SAMPLE.vir` par le nom du fichier).
*   Examiner attentivement les URL extraites pour identifier des indicateurs de compromission (IOCs) tels que des domaines suspects, des adresses IP privées ou des formats d'URL inhabituels.
*   Une analyse plus approfondie peut être nécessaire pour les fichiers ZIP intégrés dans les objets des documents RTF.

---
[Source](https://isc.sans.edu/diary/rss/32692){:target="_blank"}
