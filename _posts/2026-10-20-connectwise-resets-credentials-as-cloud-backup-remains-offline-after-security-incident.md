---
title: 'ConnectWise Resets Credentials as Cloud Backup Remains Offline After Security Incident'
date: 2026-10-20
permalink: /posts/2026/10/20/connectwise-resets-credentials-as-cloud-backup-remains-offline-after-security-incident/
tags:
- veille-cyber
- hackernews
---
### Incident de sécurité chez ConnectWise : Accès non autorisé via identifiants compromis

ConnectWise a subi une faille de sécurité ayant entraîné un accès non autorisé à des identifiants d'application liés à son service *Cloud Backup*. Par mesure de précaution, la société a suspendu ce service ainsi que *SaaS Security* et *Cloud Management*, tout en réinitialisant les accès administratifs et les identifiants applicatifs.

**Points clés :**
*   **Vecteur d'attaque :** Utilisation d'identifiants de fournisseur pour accéder aux connexions d'applications (identifiée via l'adresse IP `144.172.64.128`).
*   **Mode opératoire :** Les attaquants ont exploité les accès pour accorder des droits d'administrateur global à des applications et ajouter des secrets pour maintenir leur persistance au sein des environnements Microsoft 365.
*   **Impact :** Aucune preuve de manipulation de fichiers ou de boîtes mail n'a été constatée à ce jour. Le périmètre des clients potentiellement touchés reste en cours d'évaluation.
*   **Vulnérabilités :** Aucune CVE spécifique n'est associée à cet incident ; il s'agit d'une compromission d'identifiants d'application et d'une escalade de privilèges au sein des tenants Microsoft 365.

**Recommandations :**
*   **Ne pas reconnecter** les applications concernées avant la publication des directives officielles de restauration par ConnectWise.
*   **Auditer les tenants Microsoft 365 :** Examiner les journaux d'activité pour détecter toute activité suspecte ou création de nouveaux secrets sur les applications.
*   **Préservation des preuves :** Avant toute remédiation, conserver les logs et les preuves pertinentes pour valider l'absence d'intrusion dans vos environnements.
*   **Surveillance réseau :** Bloquer les connexions provenant des adresses IP suspectes identifiées par Huntress, notamment `144.172.64.128`.

---
[Source](https://thehackernews.com/2026/10/connectwise-resets-credentials-as-cloud.html){:target="_blank"}
