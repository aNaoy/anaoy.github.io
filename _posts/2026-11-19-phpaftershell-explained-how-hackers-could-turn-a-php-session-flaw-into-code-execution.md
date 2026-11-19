---
title: 'phpAfterShell Explained: How Hackers Could Turn a PHP Session Flaw Into Code Execution'
date: 2026-11-19
permalink: /posts/2026/11/19/phpaftershell-explained-how-hackers-could-turn-a-php-session-flaw-into-code-execution/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique phpAfterShell dans PHP

La faille **phpAfterShell** (CVE-2026-126714, score CVSS 9.2) permet à un attaquant de manipuler les sessions PHP basées sur des fichiers en interrompant brutalement l'écriture de données. En provoquant une coupure lors de l'enregistrement de la session (notamment via la fonctionnalité d'upload), l'attaquant peut injecter des objets sérialisés malveillants ou modifier des variables de session (droits d'accès, jetons CSRF) afin d'exécuter du code arbitraire sur le serveur.

**Points clés :**
*   **Mécanisme :** La vulnérabilité exploite l'absence de validation atomique lors de l'écriture des fichiers de session. Si le processus PHP est interrompu (ex: erreur de mémoire), le fichier de session conserve un mélange de données anciennes et nouvelles, permettant de corrompre la structure sérialisée.
*   **Vecteur d'attaque :** La fonctionnalité `session.upload_progress` est principalement ciblée car elle déclenche une écriture automatique dans la session avant l'exécution du code applicatif.
*   **Contexte :** Seuls les systèmes utilisant le gestionnaire de fichiers par défaut pour les sessions sont vulnérables. Les solutions comme Redis ne sont pas concernées.

**Recommandations :**
1.  **Mise à jour immédiate :** Appliquer les correctifs officiels (versions 8.2.36, 8.3.37, 8.4.28, 8.5.13 ou 8.6.0).
2.  **Mesure temporaire :** Si la mise à jour n'est pas possible, désactiver la fonctionnalité d'upload via `session.upload_progress.enabled = 0` dans le fichier `php.ini`. Attention : cela ne constitue pas une correction complète si l'application expose d'autres vecteurs d'injection dans les sessions.
3.  **Infrastructure :** Envisager le stockage des sessions dans un système de base de données externe (Redis, etc.) qui gère les remplacements de données de manière atomique.
4.  **Vérification :** Ne pas se fier uniquement au numéro de version de PHP si vous utilisez des paquets fournis par une distribution Linux, car certains correctifs peuvent être appliqués sans changement de version.

---
[Source](https://thehackernews.com/2026/11/phpaftershell-explained-how-hackers.html){:target="_blank"}
