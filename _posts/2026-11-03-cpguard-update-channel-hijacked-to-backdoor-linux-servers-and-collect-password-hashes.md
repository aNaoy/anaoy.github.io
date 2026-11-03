---
title: 'cPGuard Update Channel Hijacked to Backdoor Linux Servers and Collect Password Hashes'
date: 2026-11-03
permalink: /posts/2026/11/03/cpguard-update-channel-hijacked-to-backdoor-linux-servers-and-collect-password-hashes/
tags:
- veille-cyber
- hackernews
---
### Compromission de la chaîne de mise à jour cPGuard

Le 2 novembre, des attaquants ont piraté le système de mise à jour de l'outil de sécurité cPGuard, déployant un script malveillant sur les serveurs Linux des clients. Ce script installait une porte dérobée (*backdoor*) et exfiltrait des données sensibles vers un serveur de licences compromis.

**Points clés :**
*   **Versions affectées :** cPGuard 5.88.12 à 5.88.19.
*   **Impact :** Vol potentiel de fichiers système critiques (`/etc/shadow`, `/etc/passwd`), configurations de bases de données, historique de shell, clés SSH et fichiers *known-hosts*.
*   **État actuel :** OPSSHIELD a sécurisé son infrastructure et publié la version 5.88.25 qui supprime les éléments malveillants. 
*   **Vulnérabilité :** Aucune CVE spécifique n'a été attribuée ; il s'agit d'une attaque par compromission de chaîne d'approvisionnement (*Supply Chain Attack*) via le vol d'identifiants administratifs.

**Recommandations pour les administrateurs :**
1.  **Mise à jour immédiate :** Passer à la version 5.88.25 ou supérieure via `cpgcli update --start` et vérifier avec `cpgcli --version`.
2.  **Audit :** Vérifier les logs via `grep 'Successfully updated' /opt/cpguard/logs/install_log` pour identifier si une version compromise a été installée.
3.  **Remédiation post-compromission (obligatoire si serveur touché) :**
    *   Réinitialiser les mots de passe de tous les comptes locaux (root inclus).
    *   Renouveler tous les secrets : jetons API, mots de passe de bases de données, clés d'accès S3 et tokens (ex: DigitalOcean).
    *   Remplacer les clés privées SSH (`/root/.ssh`) et révoquer les anciennes clés publiques.
4.  **Précaution supplémentaire :** OPSSHIELD déploie une mise à jour pour supprimer les clés d'accès de support technique, par mesure de sécurité. En cas de doute sur l'intégrité du système, contacter le support de l'éditeur pour une analyse approfondie ou envisager une réinstallation du serveur.

---
[Source](https://thehackernews.com/2026/11/cpguard-update-channel-hijacked-to.html){:target="_blank"}
