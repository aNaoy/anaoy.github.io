---
title: 'Iran-Linked Hackers Disrupt U.S. Critical Infrastructure by Targeting Internet-Exposed PLCs'
date: 2026-04-08
permalink: /posts/2026/04/08/iran-linked-hackers-disrupt-us-critical-infrastructure-by-targeting-internet-exposed-plcs/
tags:
- veille-cyber
- hackernews
---
### Menaces iraniennes sur les infrastructures critiques : Ciblage des automates programmables

Des groupes de hackers liés à l'Iran intensifient leurs attaques contre les infrastructures critiques américaines, notamment dans les secteurs de l'énergie, de l'eau et des services gouvernementaux. Ces acteurs exploitent des dispositifs de technologie opérationnelle (OT) directement exposés sur Internet, comme les automates programmables (PLC), pour provoquer des dysfonctionnements, manipuler les données d'affichage (HMI/SCADA) et causer des préjudices opérationnels.

**Points clés :**
*   **Mode opératoire :** Les attaquants ciblent des automates exposés, utilisent des logiciels de configuration légitimes (ex: Rockwell Automation Studio 5000) pour établir des connexions, puis déploient le logiciel SSH *Dropbear* pour maintenir un accès à distance via le port 22.
*   **Écosystème sophistiqué :** Les activités ne se limitent pas à des pirates isolés mais s'inscrivent dans un écosystème coordonné par le ministère iranien du Renseignement (MOIS), mélangeant campagnes d'influence et cyberattaques techniques.
*   **Convergence cybercriminelle :** Des acteurs étatiques comme *MuddyWater* collaborent désormais avec des réseaux criminels (utilisant des frameworks comme *CastleRAT* ou *ChainShell*) pour brouiller les pistes et accroître leur efficacité.

**Vulnérabilités :**
*   **Exposition directe sur Internet :** Les PLC (notamment les modèles CompactLogix et Micro850) sont accessibles à distance sans protection adéquate.
*   **Absence de contrôle d'accès :** L'utilisation de configurations par défaut et l'absence d'authentification robuste facilitent l'intrusion.

**Recommandations de sécurité :**
*   **Isolement réseau :** Supprimer toute exposition directe des PLC sur Internet et placer ces équipements derrière des pare-feu ou des serveurs mandataires (proxys).
*   **Contrôle des accès :** Implémenter l'authentification multifacteur (MFA) et désactiver les fonctionnalités d'authentification inutilisées.
*   **Protection physique/logique :** Utiliser les commutateurs (physiques ou logiciels) pour empêcher toute modification à distance non autorisée.
*   **Gestion et surveillance :** Maintenir les micrologiciels (firmwares) à jour et instaurer une surveillance étroite des flux réseau pour détecter toute activité inhabituelle ou tentative de connexion SSH non sollicitée.

---
[Source](https://thehackernews.com/2026/04/iran-linked-hackers-disrupt-us-critical.html){:target="_blank"}
