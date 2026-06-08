---
title: 'Gogs patches critical zero-day enabling remote code execution'
date: 2026-06-08
permalink: /posts/2026/06/08/gogs-patches-critical-zero-day-enabling-remote-code-execution/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilité critique d'injection d'arguments dans Gogs

Gogs a corrigé une faille critique de type "zero-day" permettant une exécution de code à distance (RCE). Bien que la vulnérabilité nécessite une authentification, la configuration par défaut de Gogs (inscription ouverte et création illimitée de dépôts) permet à n'importe quel attaquant de créer un compte et d'exploiter le système sans interaction humaine, exposant ainsi plus de 2 300 instances accessibles sur Internet.

**Points clés :**
*   **Impact :** Compromission totale du serveur, lecture de dépôts privés, vol d'identifiants, mouvement latéral et altération du code source.
*   **Vecteur :** Injection d'arguments via la fonction `Merge()`.
*   **Versions affectées :** Toutes les versions jusqu'à 0.14.2 et 0.15.0+dev.
*   **Statut CVE :** En attente d'attribution.

**Recommandations :**
1.  **Mise à jour immédiate :** Passer à la version **0.14.3**, qui intègre le correctif (via le *pull request* #8301).
2.  **Mesures d'atténuation (si le patch est impossible) :**
    *   Désactiver l'inscription des utilisateurs : `DISABLE_REGISTRATION = true` dans `app.ini`.
    *   Restreindre la création de dépôts : `MAX_CREATION_LIMIT = 0` dans `app.ini` ou via le panneau d'administration.
    *   Auditer et restreindre les paramètres de fusion (*rebase merge*), bien que cela ne constitue pas une défense complète contre un utilisateur malveillant possédant des droits d'écriture.

---
[Source](https://www.bleepingcomputer.com/news/security/gogs-patches-critical-zero-day-enabling-remote-code-execution/){:target="_blank"}
