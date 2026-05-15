---
title: 'Popular node-ipc npm package compromised to steal credentials'
date: 2026-05-15
permalink: /posts/2026/05/15/popular-node-ipc-npm-package-compromised-to-steal-credentials/
tags:
- veille-cyber
- bleepingcomp
---
### Compromission du package npm node-ipc : Vol massif de données sensibles

Le package npm populaire `node-ipc` a été détourné via une attaque par chaîne d'approvisionnement. Des acteurs malveillants ont pris le contrôle du compte d'un mainteneur inactif pour injecter un malware de type « infostealer » dans plusieurs versions légitimes. Le code malveillant, hautement obfusqué, s'exécute automatiquement et exfiltre des données sensibles via des requêtes DNS TXT pour contourner les détections réseau classiques.

**Points clés :**
*   **Vecteur d'attaque :** Compromission du compte npm d'un mainteneur (« atiertant »).
*   **Mode opératoire :** Le malware scanne le système, compresse les données ciblées dans des archives temporaires, puis les exfiltre par milliers de requêtes DNS (domaine factice `sh.azurestaticprovider.net`).
*   **Volume de données :** Cible une large gamme d'identifiants (Cloud, SSH, Git, bases de données, jetons CI/CD, clés API).
*   **Discrétion :** Le malware évite les dossiers volumineux (`node_modules`, `.git`) et supprime les traces après exfiltration.

**Versions vulnérables :**
*   `node-ipc@9.1.6`
*   `node-ipc@9.2.3`
*   `node-ipc@12.0.1`

**Recommandations :**
*   **Suppression immédiate :** Désinstaller les versions compromises et mettre à jour vers une version saine.
*   **Rotation des secrets :** Considérer l'ensemble des identifiants présents sur les machines utilisant ces versions comme compromis (clés AWS, tokens GitHub, secrets CI/CD, etc.) et procéder à leur renouvellement immédiat.
*   **Audit :** Examiner les `lockfiles` et nettoyer les caches npm.
*   **Analyse forensique :** Rechercher des traces de requêtes DNS anormales vers des sous-domaines suspects dans les journaux système.

---
[Source](https://www.bleepingcomputer.com/news/security/popular-node-ipc-npm-package-compromised-to-steal-credentials/){:target="_blank"}
