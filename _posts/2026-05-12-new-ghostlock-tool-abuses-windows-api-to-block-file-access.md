---
title: 'New GhostLock tool abuses Windows API to block file access'
date: 2026-05-12
permalink: /posts/2026/05/12/new-ghostlock-tool-abuses-windows-api-to-block-file-access/
tags:
- veille-cyber
- bleepingcomp
---
### GhostLock : Une menace par déni de service via l'API Windows

L'outil « GhostLock » démontre une technique de déni de service (DoS) exploitant l'API Windows `CreateFileW` pour verrouiller l'accès aux fichiers locaux ou partagés sur le réseau (SMB). En manipulant le paramètre `dwShareMode` à zéro, un attaquant peut obtenir un accès exclusif à un fichier, empêchant tout autre utilisateur ou application de l'ouvrir et générant une erreur `STATUS_SHARING_VIOLATION`.

**Points clés :**
*   **Nature de l'attaque :** Il s'agit d'une attaque par disruption (interruption de service) et non de destruction de données.
*   **Accessibilité :** Aucun privilège d'administrateur n'est requis ; un utilisateur standard du domaine peut exécuter l'outil.
*   **Discrétion :** La technique contourne la plupart des solutions EDR et antivirus, car elle repose sur des requêtes d'ouverture de fichiers légitimes, rendant l'activité difficile à distinguer d'un usage normal.
*   **Objectif stratégique :** L'attaque peut servir de diversion pour surcharger les équipes IT et masquer d'autres activités malveillantes, comme l'exfiltration de données ou des déplacements latéraux.
*   **Réversibilité :** L'accès aux fichiers est automatiquement restauré dès que la session SMB est terminée, que les processus sont arrêtés ou que le système est redémarré.

**Vulnérabilités :**
*   Il ne s'agit pas d'une vulnérabilité logicielle classique (CVE) mais d'un abus de conception de l'API Windows (`CreateFileW`). Microsoft autorise nativement le partage exclusif pour des raisons de cohérence de données.

**Recommandations :**
*   **Surveillance spécifique :** La détection repose sur le comptage des fichiers ouverts avec `ShareAccess = 0` au niveau du serveur de stockage.
*   **Détection proactive :** Les administrateurs doivent implémenter des alertes sur les interfaces de gestion du stockage (plutôt que dans les journaux d'événements Windows ou EDR).
*   **Utilisation des ressources :** Le chercheur a mis à disposition des modèles de requêtes SIEM et des règles NDR (Network Detection and Response) dans son livre blanc pour aider les équipes de sécurité à identifier ces comportements anormaux.

---
[Source](https://www.bleepingcomputer.com/news/security/new-ghostlock-tool-abuses-windows-api-to-block-file-access/){:target="_blank"}
