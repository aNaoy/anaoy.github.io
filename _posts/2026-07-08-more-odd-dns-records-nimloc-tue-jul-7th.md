---
title: 'More Odd DNS Records: NIMLOC, (Tue, Jul 7th)'
date: 2026-07-08
permalink: /posts/2026/07/08/more-odd-dns-records-nimloc-tue-jul-7th/
tags:
- veille-cyber
- sans-isc
---
### La persistance des enregistrements DNS obsolètes : Le cas du NIMLOC

L'analyse des journaux DNS révèle fréquemment des requêtes pour des enregistrements de type 32, identifiés par l'outil Zeek comme "NIMLOC" (Nimrod Locator). Bien que ce type soit officiellement répertorié comme un protocole de routage expérimental obsolète, son apparition dans le trafic réseau moderne, notamment sur les systèmes macOS, cache une réalité différente : il s'agit d'une interprétation erronée de l'ancien protocole NetBIOS.

**Points clés :**
*   **Confusion de nomenclature :** L'IANA a assigné le type 32 à "NIMLOC", mais historiquement, ce type (ainsi que le 33) était alloué aux services NetBIOS (NB et NBSTAT) selon la RFC 1002.
*   **Héritage logiciel :** macOS continue de diffuser des annonces de noms via le port 137 en utilisant cette structure héritée, provoquant des logs trompeurs pour les outils d'analyse DNS actuels.
*   **Obsolescence :** Le protocole Nimrod n'a jamais été largement implémenté et le protocole NetBIOS est considéré comme obsolète dans les environnements Windows modernes, remplacé par le DNS et le SMB sur TCP.

**Vulnérabilités :**
*   Aucune CVE spécifique n'est associée à cet usage. Toutefois, le maintien de protocoles hérités comme NetBIOS expose les réseaux à des risques de découverte de noms par diffusion (broadcast) et d'attaques par usurpation (spoofing) au sein du segment réseau local.

**Recommandations :**
*   **Audit réseau :** Identifier et isoler les périphériques ou systèmes d'exploitation qui continuent d'utiliser NetBIOS.
*   **Désactivation :** Dans les environnements sécurisés, désactiver les services NetBIOS sur TCP/IP s'ils ne sont pas strictement nécessaires au fonctionnement d'applications legacy.
*   **Configuration de journalisation :** Prendre en compte cette discordance lors de l'analyse des journaux DNS (notamment avec Zeek) pour éviter de classer à tort ce trafic comme une tentative d'utilisation du protocole Nimrod.

---
[Source](https://isc.sans.edu/diary/rss/33128){:target="_blank"}
