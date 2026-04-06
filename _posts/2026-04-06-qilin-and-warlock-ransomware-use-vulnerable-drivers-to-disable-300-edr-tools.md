---
title: 'Qilin and Warlock Ransomware Use Vulnerable Drivers to Disable 300+ EDR Tools'
date: 2026-04-06
permalink: /posts/2026/04/06/qilin-and-warlock-ransomware-use-vulnerable-drivers-to-disable-300-edr-tools/
tags:
- veille-cyber
- hackernews
---
### Neutralisation des solutions de sécurité par les ransomwares Qilin et Warlock via la technique BYOVD

Les groupes de ransomware Qilin et Warlock exploitent des pilotes vulnérables légitimes pour désactiver plus de 300 solutions EDR (Endpoint Detection and Response) à travers une attaque de type « Bring Your Own Vulnerable Driver » (BYOVD).

**Points clés :**
*   **Mode opératoire :** Utilisation de DLL malveillantes (chargées via DLL side-loading) pour neutraliser les hooks utilisateur, masquer les logs ETW et charger en mémoire des pilotes compromis.
*   **Outils de désactivation :**
    *   **Qilin :** Utilise `rwdrv.sys` (version renommée de *ThrottleStop.sys*) pour un accès au noyau et `hlpdrv.sys` pour arrêter les processus EDR.
    *   **Warlock :** Exploite le pilote `NSecKrnl.sys` et recourt à divers outils pour le mouvement latéral et l'exfiltration (PsExec, Velociraptor, Rclone, serveurs mandataires via Yuze).
*   **Vulnérabilités :** L'attaque repose sur l'exploitation de pilotes tiers officiels possédant des vulnérabilités connues (BYOVD). Bien que les pilotes spécifiques ne soient pas listés avec un identifiant CVE unique dans l'article, la technique cible les faiblesses inhérentes à la gestion des privilèges kernel.
*   **Stratégie :** L'exécution du ransomware survient en moyenne six jours après l'accès initial, obtenu principalement via le vol d'identifiants.

**Recommandations :**
*   **Gouvernance des pilotes :** N'autoriser que les pilotes signés provenant d'éditeurs strictement approuvés via des politiques de contrôle d'application.
*   **Surveillance renforcée :** Surveiller activement les événements d'installation de pilotes et l'activité au niveau du noyau (kernel).
*   **Gestion des correctifs :** Maintenir une politique rigoureuse de mise à jour, particulièrement pour les logiciels de sécurité.
*   **Défense multicouche :** Passer d'une protection EDR classique vers des solutions intégrant une intégrité stricte du noyau et une surveillance temps réel des activités système critiques.

---
[Source](https://thehackernews.com/2026/04/qilin-and-warlock-ransomware-use.html){:target="_blank"}
