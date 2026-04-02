---
title: 'New Progress ShareFile flaws can be chained in pre-auth RCE attacks'
date: 2026-04-02
permalink: /posts/2026/04/02/new-progress-sharefile-flaws-can-be-chained-in-pre-auth-rce-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilités critiques dans Progress ShareFile : Chaînage d'exploits pour une exécution de code à distance

Une chaîne d'exploits critiques a été identifiée dans le composant *Storage Zones Controller* (SZC) de Progress ShareFile (branche 5.x). Cette vulnérabilité permet à un attaquant non authentifié de prendre le contrôle total des serveurs exposés.

**Points clés :**
*   **Vecteur d'attaque :** La combinaison de deux vulnérabilités permet de contourner l'authentification, puis d'exécuter du code arbitraire.
*   **Exposition :** Environ 700 instances sont actuellement identifiées comme exposées sur Internet, principalement aux États-Unis et en Europe.
*   **Risque :** Bien qu'aucune exploitation active ne soit encore observée, la publication des détails techniques rend une attaque par des groupes de ransomware hautement probable.

**Vulnérabilités :**
*   **CVE-2026-2699 (Contournement d'authentification) :** Une mauvaise gestion des redirections HTTP permet d'accéder à l'interface d'administration.
*   **CVE-2026-2701 (Exécution de code à distance) :** En modifiant les configurations de zones de stockage, un attaquant peut téléverser des webshells ASPX dans la racine web de l'application.

**Recommandations :**
*   **Mise à jour immédiate :** Appliquer sans délai le correctif de sécurité en passant à la version **5.12.4** (publiée le 10 mars).
*   **Audit de sécurité :** Vérifier les configurations des zones de stockage et surveiller les journaux d'accès pour détecter toute activité suspecte ou création de fichiers non autorisée dans le répertoire racine de l'application.

---
[Source](https://www.bleepingcomputer.com/news/security/new-progress-sharefile-flaws-can-be-chained-in-pre-auth-rce-attacks/){:target="_blank"}
