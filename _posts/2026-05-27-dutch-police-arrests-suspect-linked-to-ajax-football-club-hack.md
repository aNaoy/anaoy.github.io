---
title: 'Dutch police arrests suspect linked to Ajax football club hack'
date: 2026-05-27
permalink: /posts/2026/05/27/dutch-police-arrests-suspect-linked-to-ajax-football-club-hack/
tags:
- veille-cyber
- bleepingcomp
---
### Arrestation liée à la cyberattaque de l'Ajax Amsterdam

La police néerlandaise a arrêté un homme de 35 ans soupçonné d'avoir infiltré à plusieurs reprises les systèmes informatiques de l'AFC Ajax début 2026. L'individu a exploité des vulnérabilités critiques pour accéder aux données personnelles de plus de 300 000 comptes, manipuler des interdictions de stade et transférer frauduleusement des billets de saison.

**Points clés :**
*   **Incident :** Accès non autorisé aux systèmes d'information du club de football Ajax Amsterdam.
*   **Impact :** Exposition des données de centaines de personnes, modification de 538 interdictions de stade et accès à 42 000 billets de saison.
*   **Modus operandi :** Exploitation de failles de sécurité via des API et des clés partagées pour manipuler les bases de données des supporters.

**Vulnérabilités :**
*   L'article ne mentionne pas de CVE spécifique, mais pointe des **failles critiques au niveau des API** et une **mauvaise gestion des clés d'accès partagées**, permettant une escalade des privilèges et une manipulation massive de données.

**Recommandations :**
*   **Sécurisation des API :** Mettre en œuvre une authentification robuste et des contrôles d'accès stricts sur toutes les interfaces de programmation.
*   **Gestion des clés :** Bannir l'usage de clés d'accès partagées et privilégier des jetons individuels à durée de vie limitée.
*   **Audit et validation :** Réaliser des tests d'intrusion réguliers pour valider non seulement la pénétration, mais aussi l'efficacité des règles de détection et des configurations cloud.
*   **Protection des données :** Appliquer le principe du moindre privilège pour limiter l'impact en cas de compromission d'un compte.

---
[Source](https://www.bleepingcomputer.com/news/security/dutch-police-arrests-suspect-linked-to-ajax-football-club-hack/){:target="_blank"}
