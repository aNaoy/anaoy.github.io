---
title: 'PTC warns of imminent threat from critical Windchill, FlexPLM RCE bug'
date: 2026-03-25
permalink: /posts/2026/03/25/ptc-warns-of-imminent-threat-from-critical-windchill-flexplm-rce-bug/
tags:
- veille-cyber
- bleepingcomp
---
### Menace critique sur les solutions PTC Windchill et FlexPLM

Une vulnérabilité critique affectant les solutions de gestion du cycle de vie des produits (PLM) PTC Windchill et FlexPLM fait l'objet d'une alerte urgente, en raison d'une menace d'exploitation imminente jugée suffisamment sérieuse pour mobiliser les autorités fédérales allemandes (BKA).

**Vulnérabilité identifiée :**
*   **CVE-2026-4681 :** Une faille de type exécution de code à distance (RCE) via la désérialisation de données de confiance. Elle touche la quasi-totalité des versions supportées des logiciels.

**Points clés :**
*   **Urgence nationale :** Les autorités allemandes ont directement contacté les entreprises utilisatrices, y compris à leur domicile, pour les alerter des risques d'espionnage industriel sur des secteurs stratégiques.
*   **Absence de correctif :** PTC développe actuellement des patchs de sécurité ; aucun correctif officiel n'est disponible à ce jour.
*   **Indicateurs de compromission (IoC) :** PTC a publié des éléments techniques pour détecter une éventuelle exploitation, notamment la présence de fichiers suspects (ex: `GW.class`, `dpr_<random>.jsp`) ou des requêtes inhabituelles vers les serveurs.

**Recommandations :**
*   **Application immédiate d'une règle de filtrage :** Déployer la règle Apache/IIS fournie par PTC pour bloquer l'accès au chemin du servlet vulnérable (cette mesure n'affecte pas les fonctionnalités du système). Cette règle doit être appliquée sur tous les serveurs, y compris ceux qui ne sont pas exposés sur Internet.
*   **Isolation temporaire :** Si le filtrage est impossible, il est vivement recommandé de déconnecter les instances vulnérables d'Internet ou de suspendre le service.
*   **Surveillance :** Analyser les logs à la recherche des IoC fournis par l'éditeur pour identifier toute tentative d'exploitation ou de pré-compromission déjà effectuée.

---
[Source](https://www.bleepingcomputer.com/news/security/ptc-warns-of-imminent-threat-from-critical-windchill-flexplm-rce-bug/){:target="_blank"}
