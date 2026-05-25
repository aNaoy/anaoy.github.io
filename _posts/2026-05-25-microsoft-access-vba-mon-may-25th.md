---
title: 'Microsoft Access VBA, (Mon, May 25th)'
date: 2026-05-25
permalink: /posts/2026/05/25/microsoft-access-vba-mon-may-25th/
tags:
- veille-cyber
- sans-isc
---
### Analyse et extraction du code VBA dans les fichiers Microsoft Access

Les fichiers Microsoft Access (.accdb) ne suivent pas les structures standards (OLE ou OOXML), rendant les outils d'analyse habituels comme `oledump.py` inefficaces. L'absence de documentation officielle de Microsoft sur ce format complique l'extraction malveillante du code VBA.

**Points clés :**
* **Structure propriétaire :** Contrairement aux autres fichiers Office, les fichiers Access ne contiennent pas d'objets OLE incorporés, nécessitant des méthodes d'analyse spécifiques.
* **Compression VBA :** Le code VBA au sein de ces fichiers est compressé au format ZLIB.
* **Nouvel outil d'analyse :** L'outil `search-for-compression.py` a été mis à jour (option `-t`) pour identifier et décompresser les flux VBA dans les fichiers Access.
* **Extraction :** Le processus permet d'extraire deux types de flux : les flux de métadonnées (propriétés du projet, références) et le code source VBA brut.

**Vulnérabilités :**
* Aucune CVE spécifique n'est mentionnée, mais le format Access constitue un vecteur d'occultation efficace pour les attaquants souhaitant dissimuler du code malveillant aux outils de détection statique classiques.

**Recommandations :**
* **Mise à jour des outils :** Intégrer `search-for-compression.py` dans les pipelines d'analyse de fichiers suspects.
* **Analyse approfondie :** Ne pas se limiter aux outils d'analyse OLE traditionnels pour les fichiers de base de données. Rechercher systématiquement les flux compressés (ZLIB) pour isoler les macros VBA potentiellement malveillantes.
* **Veille technique :** Suivre les travaux de Didier Stevens pour l'évolution des techniques de décompilation des formats de fichiers opaques de Microsoft.

---
[Source](https://isc.sans.edu/diary/rss/33012){:target="_blank"}
