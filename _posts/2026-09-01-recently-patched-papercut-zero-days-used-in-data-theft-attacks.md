---
title: 'Recently patched PaperCut zero-days used in data theft attacks'
date: 2026-09-01
permalink: /posts/2026/09/01/recently-patched-papercut-zero-days-used-in-data-theft-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Exploitation active des vulnérabilités critiques dans PaperCut

Les logiciels de gestion d'impression PaperCut NG et MF sont actuellement la cible d'attaques exploitant deux vulnérabilités critiques. Ces failles, initialement identifiées comme des vulnérabilités « zero-day », sont utilisées par des acteurs malveillants pour contourner l'authentification et exfiltrer des données sensibles depuis les bases de données des serveurs compromis.

**Points clés :**
*   **Impact :** Environ 70 000 organisations (entreprises, agences gouvernementales, institutions éducatives) utilisent ces logiciels.
*   **Nature des attaques :** Les attaquants exploitent les failles pour intercepter les recherches d'utilisateurs externes et extraire des tables de bases de données (via Derby).
*   **Historique :** Les solutions PaperCut sont régulièrement ciblées par des groupes de ransomware et des acteurs étatiques en raison de leur large exposition sur Internet.

**Vulnérabilités :**
*   **CVE-2026-81578** et **CVE-2026-82078** : Le chaînage de ces deux vulnérabilités permet de contourner l'authentification et d'exécuter du code à distance (RCE) sur les serveurs vulnérables.

**Recommandations :**
*   **Mise à jour immédiate :** Tous les clients utilisant des serveurs accessibles sur Internet doivent installer la **"Release 3"** (la troisième série de correctifs d'urgence), même si des correctifs précédents ont déjà été appliqués.
*   **Surveillance :** Consulter le bulletin de sécurité officiel de PaperCut pour examiner les indicateurs de compromission (IoC) fournis et vérifier l'intégrité des serveurs.
*   **Isolation :** Si l'application des correctifs n'est pas immédiatement possible, il est fortement recommandé de retirer les serveurs de l'exposition directe sur Internet.

---
[Source](https://www.bleepingcomputer.com/news/security/recently-patched-papercut-zero-days-used-in-data-theft-attacks/){:target="_blank"}
