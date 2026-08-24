---
title: 'DOUBLECUPs PNG Payload, (Mon, Aug 24th)'
date: 2026-08-24
permalink: /posts/2026/08/24/doublecups-png-payload-mon-aug-24th/
tags:
- veille-cyber
- sans-isc
---
### Analyse de la charge utile DOUBLECUP

Le malware DOUBLECUP utilise une technique simpliste mais efficace pour dissimuler des scripts PowerShell malveillants au sein de fichiers images PNG. Contrairement à la stéganographie traditionnelle, aucune donnée n'est encodée dans les pixels ou les métadonnées ; le script est simplement ajouté à la fin du fichier image.

**Points clés :**
* **Technique de dissimulation :** Le code malveillant est concaténé après les données binaires du fichier PNG.
* **Astuce d'exécution :** Le script PowerShell commence par les caractères `0x0D 0x0A` (CRLF), permettant de délimiter proprement la charge utile.
* **Extraction simplifiée :** L'utilisation de la commande native Windows `findstr` suffit à isoler et extraire le script du fichier image, lequel peut ensuite être directement redirigé vers l'interpréteur PowerShell.

**Vulnérabilités :**
* Aucune CVE spécifique n'est associée, car cette technique exploite l'utilisation légitime des outils système (Living off the Land) et la capacité du shell Windows à traiter des fichiers hybrides.

**Recommandations :**
* **Surveillance des processus :** Surveiller l'utilisation de `findstr` couplé à une redirection vers `powershell.exe` au sein des logs système.
* **Analyse de fichiers :** Ne pas se fier à l'extension de fichier ou à la validité apparente d'une image. Effectuer une analyse heuristique sur le contenu des fichiers téléchargés pour détecter des données ajoutées après le marqueur de fin de fichier (`IEND` pour les PNG).
* **Restrictions PowerShell :** Appliquer une politique d'exécution stricte (Constrained Language Mode) et utiliser la journalisation des blocs de script pour identifier les exécutions malveillantes.

---
[Source](https://isc.sans.edu/diary/rss/33274){:target="_blank"}
