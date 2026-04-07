---
title: 'US warns of Iranian hackers targeting critical infrastructure'
date: 2026-04-07
permalink: /posts/2026/04/07/us-warns-of-iranian-hackers-targeting-critical-infrastructure/
tags:
- veille-cyber
- bleepingcomp
---
### Menaces iraniennes sur les infrastructures critiques américaines

Des agences fédérales américaines (FBI, CISA, NSA, etc.) ont émis une alerte concernant une campagne de cyberattaques menée par des groupes affiliés à l'Iran ciblant les infrastructures critiques (énergie, eau, services gouvernementaux). Ces attaques, qui ont causé des perturbations opérationnelles et des pertes financières depuis mars 2026, exploitent des automates programmables industriels (PLC) exposés sur Internet.

**Points clés :**
*   **Cibles :** Les automates Rockwell/Allen-Bradley connectés directement au web.
*   **Mode opératoire :** Les attaquants extraient des fichiers de projet et manipulent les données affichées sur les interfaces homme-machine (IHM) et les systèmes SCADA pour créer des dysfonctionnements.
*   **Contexte :** Cette escalade des activités est liée aux tensions géopolitiques entre l'Iran, les États-Unis et Israël.
*   **Antécédents :** Une menace similaire avait été identifiée en 2023 avec le groupe *CyberAv3ngers*, qui avait compromis des systèmes Unitronics.

**Vulnérabilités :**
*   Exposition directe des dispositifs OT (Operational Technology) sur Internet.
*   Utilisation de configurations par défaut ou d'authentifications faibles.
*   Absence de segmentation réseau adéquate.
*(Note : Bien que le rapport mentionne des cibles spécifiques, aucune CVE spécifique n'est citée dans l'article, l'exploitation reposant principalement sur l'exposition réseau et des méthodes d'accès non sécurisées).*

**Recommandations :**
*   **Isolement :** Déconnecter impérativement les automates (PLC) de l'Internet ou les placer derrière un pare-feu robuste.
*   **Sécurisation des accès :** Implémenter l'authentification multifacteur (MFA) pour tout accès au réseau OT.
*   **Durcissement :** Désactiver les services inutilisés et supprimer les clés d'authentification par défaut.
*   **Maintenance :** Mettre à jour les micrologiciels (firmware) des équipements vers les dernières versions.
*   **Surveillance :** Analyser le trafic réseau à la recherche d'activités suspectes (particulièrement en provenance de fournisseurs d'hébergement étrangers) et auditer les journaux pour détecter des indicateurs de compromission.

---
[Source](https://www.bleepingcomputer.com/news/security/us-warns-of-iranian-hackers-targeting-critical-infrastructure/){:target="_blank"}
