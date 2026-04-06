---
title: 'DPRK-Linked Hackers Use GitHub as C2 in Multi-Stage Attacks Targeting South Korea'
date: 2026-04-06
permalink: /posts/2026/04/06/dprk-linked-hackers-use-github-as-c2-in-multi-stage-attacks-targeting-south-korea/
tags:
- veille-cyber
- hackernews
---
### Infiltration via GitHub : La stratégie de cyberespionnage du groupe Kimsuky

Le groupe de hackers nord-coréens Kimsuky mène des campagnes de cyberespionnage sophistiquées ciblant des organisations sud-coréennes. Ces attaques se distinguent par l'utilisation de services légitimes et d'outils natifs Windows (LolBins) pour masquer leurs activités.

**Points clés :**
*   **Vecteur d'attaque :** Distribution via des emails de phishing contenant des raccourcis Windows (LNK) malveillants.
*   **Infrastructure C2 :** Détournement de GitHub pour la commande et le contrôle (exfiltration de données et réception d'instructions), tirant parti de la confiance accordée à cette plateforme pour éviter la détection.
*   **Persistance :** Utilisation de tâches planifiées exécutant des scripts PowerShell/VBScript toutes les 30 minutes.
*   **Techniques d'évasion :** Les scripts détectent les environnements de virtualisation et de débogage pour s'auto-terminer si une analyse est suspectée.
*   **Polyvalence :** Utilisation de divers malwares, notamment Xeno RAT, MoonPeak, ainsi que des backdoors basées sur Python et le cheval de Troie RokRAT (via side-loading de DLL).

**Vulnérabilités exploitées :**
*   Aucune CVE spécifique n'est mentionnée ; les attaquants exploitent les fonctionnalités natives du système d'exploitation et des services Cloud (GitHub, Dropbox) plutôt que des failles logicielles documentées.

**Recommandations :**
*   **Surveillance des logs :** Surveiller étroitement l'exécution de scripts PowerShell suspects, particulièrement ceux configurés comme tâches planifiées persistantes ou utilisant des réseaux externes non autorisés.
*   **Filtrage des emails :** Renforcer les politiques de filtrage des pièces jointes, en bloquant ou en inspectant systématiquement les fichiers LNK et les macros Office.
*   **Restrictions LolBins :** Limiter l'exécution de PowerShell et d'autres outils d'administration système (LolBins) via des politiques de contrôle d'application (AppLocker ou Windows Defender Application Control) pour les utilisateurs non autorisés.
*   **Analyse comportementale :** Déployer des solutions EDR capables de détecter les comportements anormaux, tels que la création de tâches planifiées masquées ou les connexions inhabituelles vers des dépôts publics GitHub à partir de postes de travail internes.

---
[Source](https://thehackernews.com/2026/04/dprk-linked-hackers-use-github-as-c2-in.html){:target="_blank"}
