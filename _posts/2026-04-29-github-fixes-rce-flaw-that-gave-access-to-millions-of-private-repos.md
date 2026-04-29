---
title: 'GitHub fixes RCE flaw that gave access to millions of private repos'
date: 2026-04-29
permalink: /posts/2026/04/29/github-fixes-rce-flaw-that-gave-access-to-millions-of-private-repos/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilité critique RCE : GitHub sécurise ses serveurs

Une faille critique d'exécution de code à distance (RCE) a été découverte et corrigée sur les plateformes GitHub. Bien que potentiellement dévastatrice, aucune exploitation malveillante n'a été détectée avant la publication du correctif.

**Points clés :**
*   **Découverte :** Identifiée par les chercheurs de Wiz via le programme de bug bounty de GitHub.
*   **Impact :** Permettait à un attaquant disposant d'un accès en écriture sur un dépôt de prendre le contrôle total du serveur, d'accéder aux dépôts privés et de compromettre des secrets internes.
*   **Réactivité :** GitHub a déployé un correctif sur GitHub.com en moins de deux heures après le signalement.
*   **État actuel :** 88 % des instances GitHub Enterprise Server (GHES) accessibles publiquement resteraient vulnérables.

**Vulnérabilité identifiée :**
*   **CVE-2026-3854 :** Défaut de désinfection des métadonnées lors des opérations `git push`. L'injection de valeurs malveillantes permettait de contourner le bac à sable (sandboxing) et d'exécuter du code arbitraire sur les nœuds de stockage partagés ou les serveurs Enterprise.

**Recommandations :**
*   **Administrateurs GHES :** Mise à jour immédiate vers les versions corrigées (3.14.25, 3.15.20, 3.16.16, 3.17.13, 3.18.8, 3.19.4, 3.20.0 ou versions ultérieures).
*   **Vérification :** Appliquer les correctifs officiels fournis par GitHub pour sécuriser les instances auto-hébergées.

---
[Source](https://www.bleepingcomputer.com/news/security/github-fixes-rce-flaw-that-gave-access-to-millions-of-private-repos/){:target="_blank"}
