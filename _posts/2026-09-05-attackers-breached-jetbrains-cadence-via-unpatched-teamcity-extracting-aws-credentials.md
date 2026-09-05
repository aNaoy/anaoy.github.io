---
title: 'Attackers Breached JetBrains Cadence via Unpatched TeamCity, Extracting AWS Credentials'
date: 2026-09-05
permalink: /posts/2026/09/05/attackers-breached-jetbrains-cadence-via-unpatched-teamcity-extracting-aws-credentials/
tags:
- veille-cyber
- hackernews
---
### Compromission de JetBrains Cadence via une vulnérabilité TeamCity

**Points clés :**
*   Entre le 8 et le 24 août 2026, des attaquants ont infiltré le service cloud JetBrains Cadence en exploitant un serveur TeamCity non patché.
*   Les pirates ont accédé à des sauvegardes serveur (2024), exposant des données personnelles, du code source, des clés AWS et des configurations.
*   Le serveur cible (`api.cadence.jetbrains.com`) a été mis hors ligne suite à la découverte de l'intrusion.
*   L'incident fait peser des risques accrus de phishing, d'usurpation d'identité et d'accès non autorisé aux environnements cloud des utilisateurs.

**Vulnérabilité :**
*   **CVE-2026-63077 (CVSS 9.8) :** Une faille de désérialisation de données non fiables permettant à un attaquant non authentifié d'exécuter des commandes arbitraires avec les privilèges du processus serveur TeamCity.

**Recommandations pour les utilisateurs :**
*   **Réinitialisation immédiate :** Révoquer et renouveler tous les identifiants, secrets, jetons d'accès, clés SSH et API potentiellement stockés ou utilisés via Cadence.
*   **Audit de sécurité :** Vérifier les comptes AWS, les buckets S3, les dépôts de code et les environnements de déploiement à la recherche de modifications suspectes ou d'activités inhabituelles depuis le 8 août 2026.
*   **Gestion des risques :** Considérer toutes les exécutions passées, ainsi que leurs entrées/sorties, comme compromises et potentiellement non fiables.
*   **Vigilance accrue :** Être particulièrement attentif aux tentatives de phishing ciblé utilisant les informations personnelles exposées.

---
[Source](https://thehackernews.com/2026/09/attackers-breached-jetbrains-cadence.html){:target="_blank"}
