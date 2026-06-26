---
title: 'Anthropic is testing desktop-like Claude Cowork for mobile'
date: 2026-06-26
permalink: /posts/2026/06/26/anthropic-is-testing-desktop-like-claude-cowork-for-mobile/
tags:
- veille-cyber
- bleepingcomp
---
### Extension de Claude Cowork aux appareils mobiles

Anthropic prépare le déploiement de **Claude Cowork** sur mobile, permettant aux utilisateurs de piloter à distance leurs agents IA exécutés sur ordinateur. Cette fonctionnalité offre un suivi en temps réel et la gestion de tâches complexes (traitement de documents, organisation de fichiers, automatisation) même lorsque l'application mobile est fermée.

**Points clés :**
*   **Architecture déportée :** Le mobile sert de « télécommande ». Le traitement intensif et l'accès aux fichiers locaux restent cantonnés à la machine hôte (macOS ou Windows).
*   **Continuité :** La persistance des tâches permet de lancer des processus longs sur PC et d'en suivre l'évolution depuis un smartphone.
*   **Usage polyvalent :** Contrairement à *Claude Code* (orienté développement), *Cowork* est conçu pour des tâches administratives et la gestion de fichiers.

**Vulnérabilités et sécurité :**
*   L'article ne mentionne aucune CVE spécifique associée à cette phase de test.
*   **Risque lié aux agents :** L'octroi d'un accès aux fichiers locaux à un agent IA, couplé à une interface de contrôle mobile, augmente la surface d'attaque en cas de compromission du compte utilisateur ou de l'appareil mobile (accès distant non autorisé à des données sensibles).

**Recommandations :**
*   **Principe du moindre privilège :** Restreindre rigoureusement les dossiers et partitions auxquels l'agent Claude Cowork a accès sur la machine hôte.
*   **Sécurisation des accès :** Activer l'authentification multifacteur (MFA) sur le compte Anthropic pour prévenir tout contrôle non autorisé de l'agent via l'interface mobile.
*   **Surveillance :** Maintenir une supervision active des activités de l'agent sur la machine hôte lors de l'exécution de processus en arrière-plan.

---
[Source](https://www.bleepingcomputer.com/news/artificial-intelligence/anthropic-is-testing-desktop-like-claude-cowork-for-mobile/){:target="_blank"}
