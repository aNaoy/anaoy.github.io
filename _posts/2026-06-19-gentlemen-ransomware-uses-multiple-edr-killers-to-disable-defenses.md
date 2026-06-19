---
title: 'Gentlemen ransomware uses multiple EDR killers to disable defenses'
date: 2026-06-19
permalink: /posts/2026/06/19/gentlemen-ransomware-uses-multiple-edr-killers-to-disable-defenses/
tags:
- veille-cyber
- bleepingcomp
---
### Gentlemen Ransomware : L'arsenal de neutralisation des EDR

Le groupe de ransomware-as-a-service (RaaS) « Gentlemen » a développé une suite d'outils sophistiqués, baptisée « GentleKiller », pour désactiver les solutions de détection et de réponse aux points de terminaison (EDR) avant le déploiement de ses charges utiles. Ce cadre modulaire permet au groupe de neutraliser plus de 400 processus liés à environ 48 fournisseurs de sécurité majeurs (dont CrowdStrike, SentinelOne, Microsoft et ESET).

**Points clés :**
*   **Technique BYOVD (Bring Your Own Vulnerable Driver) :** Les outils utilisent des pilotes légitimes mais vulnérables pour obtenir des privilèges au niveau du noyau (kernel) et forcer l'arrêt des services de sécurité.
*   **Modularité :** Le framework est conçu pour permettre une mise à jour rapide des pilotes vulnérables utilisés sans refonte majeure du code.
*   **Diversification :** En complément de GentleKiller, le groupe utilise d'autres outils d'extinction d'EDR tels que HexKiller, ThrottleBlood et HavocKiller pour assurer une redondance.
*   **Ciblage stratégique :** Le groupe sélectionne ses victimes en fonction de la configuration de leurs terminaux FortiGate, profitant potentiellement de fuites d'identifiants VPN massives.
*   **Obfuscation :** Les binaires sont protégés par des outils commerciaux (Enigma, Themida) et utilisent des signatures numériques volées pour tromper les analyses initiales.

**Vulnérabilités :**
L'article ne mentionne pas de CVE spécifique, mais souligne que la méthode repose sur l'exploitation systématique de **pilotes tiers vulnérables** chargés dans le système d'exploitation pour élever les privilèges au niveau du noyau.

**Recommandations :**
*   **Durcissement de la liste d'autorisation des pilotes :** Implémenter une politique stricte (via le contrôle d'application ou la protection de l'intégrité du code par hyperviseur - HVCI) pour bloquer le chargement de pilotes non signés ou connus pour être vulnérables.
*   **Surveillance accrue des terminaux :** Détecter les tentatives anormales d'arrêt des services de sécurité critiques ou l'utilisation de pilotes inhabituels par des processus non autorisés.
*   **Gestion des accès VPN :** Sécuriser les accès FortiGate par une authentification multi-facteurs (MFA) robuste, en tenant compte des risques liés aux fuites d'identifiants ("FortiBleed").
*   **Mise à jour des systèmes :** S'assurer que les correctifs de sécurité pour les VPN et les infrastructures périmétriques sont appliqués pour limiter le point d'entrée initial des attaquants.

---
[Source](https://www.bleepingcomputer.com/news/security/gentlemen-ransomware-uses-multiple-edr-killers-to-disable-defenses/){:target="_blank"}
