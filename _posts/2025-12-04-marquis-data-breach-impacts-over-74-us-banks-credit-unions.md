---
title: 'Marquis data breach impacts over 74 US banks, credit unions'
date: 2025-12-04
permalink: /posts/2025/12/04/marquis-data-breach-impacts-over-74-us-banks-credit-unions/
tags:
- veille-cyber
- bleepingcomp
---
## Piratage de Marquis Software : 74 banques et coopératives de crédit américaines touchées

Le fournisseur de logiciels financiers Marquis Software Solutions a subi une violation de données résultant d'une attaque par ransomware le 14 août 2025. L'intrusion a eu lieu par le biais de son pare-feu SonicWall, permettant aux attaquants de dérober des fichiers contenant des informations personnelles de clients de ses entreprises partenaires. Au moins 74 institutions financières, incluant des banques et des coopératives de crédit à travers les États-Unis, sont impactées, affectant potentiellement plus de 400 000 clients. Les données compromises peuvent inclure noms, adresses, numéros de téléphone, numéros de sécurité sociale, identifiants fiscaux, informations de compte bancaire (sans codes d'accès) et dates de naissance.

**Points clés :**

*   **Fournisseur affecté :** Marquis Software Solutions, qui propose des services d'analyse de données, de CRM, de conformité et de marketing numérique à plus de 700 institutions financières.
*   **Type d'attaque :** Ransomware.
*   **Date de l'incident :** 14 août 2025.
*   **Vecteur d'attaque initial :** Pare-feu SonicWall.
*   **Entités touchées :** 74 banques et coopératives de crédit américaines.
*   **Volume de données :** Informations personnelles de plus de 400 000 clients.
*   **Absence de preuves de mauvaise utilisation actuelle :** Marquis affirme qu'il n'y a aucune preuve que les données aient été exploitées ou publiées. Cependant, une information non confirmée suggère que Marquis aurait payé une rançon.

**Vulnérabilités suspectées :**

*   **CVE-2024-40766 :** Une vulnérabilité critique dans les dispositifs SonicWall SSL VPN qui permettait aux attaquants de voler des identifiants et des codes à usage unique (OTP).
*   **Exploitation des identifiants volés :** Même après le correctif de SonicWall, les attaquants ont continué à accéder aux systèmes en utilisant des identifiants VPN précédemment dérobés.
*   **Contournement de l'authentification multifacteur (MFA) :** Des rapports suggèrent que les attaquants ont pu accéder à des comptes SonicWall VPN protégés par MFA, potentiellement en exploitant les graines OTP volées lors d'exploitations antérieures.

**Recommandations adoptées par Marquis (suite à l'incident) :**

*   Mise à jour et application de correctifs sur tous les dispositifs pare-feu.
*   Rotation des mots de passe pour les comptes locaux.
*   Suppression des comptes anciens ou inutilisés.
*   Activation de l'authentification multifacteur pour tous les comptes de pare-feu et VPN.
*   Augmentation de la rétention des journaux pour les dispositifs pare-feu.
*   Application de politiques de verrouillage de compte pour les tentatives de connexion VPN infructueuses.
*   Mise en place de filtrage géographique (geo-IP) pour autoriser les connexions uniquement depuis des pays nécessaires.
*   Application de politiques pour bloquer automatiquement les connexions vers/depuis des serveurs de commandement et de contrôle de botnet connus au niveau du pare-feu.

---
[Source](https://www.bleepingcomputer.com/news/security/marquis-data-breach-impacts-over-74-us-banks-credit-unions/){:target="_blank"}
