---
title: 'GitHub Account Compromise Led to Salesloft Drift Breach Affecting 22 Companies'
date: 2025-09-08
permalink: /posts/2025/09/08/github-account-compromise-led-to-salesloft-drift-breach-affecting-22-companies/
tags:
- veille-cyber
- hackernews
---
**Compromission de GitHub chez Salesloft et impact sur Drift**

Une attaque par la chaîne d'approvisionnement a débuté par le compromis d'un compte GitHub chez Salesloft, permettant à un acteur malveillant d'accéder à plusieurs dépôts entre mars et juin 2025. L'attaquant a pu télécharger du contenu, ajouter un utilisateur invité et configurer des flux de travail. Par la suite, l'environnement Amazon Web Services (AWS) de l'application Drift a été accédé, et des jetons OAuth dérobés ont été utilisés pour extraire des données via les intégrations de Drift avec les clients. 22 entreprises ont confirmé avoir été affectées par cette brèche.

**Points clés :**

*   Compromission initiale d'un compte GitHub chez Salesloft.
*   Accès aux dépôts et modification de configurations.
*   Accès à l'environnement AWS de Drift et vol de jetons OAuth clients.
*   Utilisation des jetons OAuth pour accéder aux données via des intégrations tierces.
*   Impact sur 22 entreprises clientes.

**Vulnérabilités :**

Bien que l'article ne mentionne pas de CVE spécifiques, la vulnérabilité réside dans la sécurisation insuffisante du compte GitHub, permettant un accès non autorisé et des actions malveillantes. L'obtention de jetons OAuth client via l'environnement AWS suggère également une faiblesse dans la gestion des autorisations et des secrets pour les intégrations externes.

**Recommandations :**

*   Les applications tierces intégrées à Drift via clé API doivent révoquer proactivement leurs clés existantes.
*   Salesloft a isolé l'infrastructure Drift, mis l'application hors ligne, fait pivoter les identifiants et renforcé l'environnement avec des contrôles de segmentation améliorés entre Salesloft et Drift.
*   Salesforce a rétabli ses intégrations avec Salesloft, à l'exception de Drift, qui reste désactivée jusqu'à nouvel ordre.

---
[Source](https://thehackernews.com/2025/09/github-account-compromise-led-to.html){:target="_blank"}
