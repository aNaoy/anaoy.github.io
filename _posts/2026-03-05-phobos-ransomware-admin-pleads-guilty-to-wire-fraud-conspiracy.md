---
title: 'Phobos ransomware admin pleads guilty to wire fraud conspiracy'
date: 2026-03-05
permalink: /posts/2026/03/05/phobos-ransomware-admin-pleads-guilty-to-wire-fraud-conspiracy/
tags:
- veille-cyber
- bleepingcomp
---
### Condamnation d'un administrateur clé du ransomware Phobos

Evgenii Ptitsyn, un ressortissant russe, a plaidé coupable devant la justice américaine pour son rôle central dans l'administration du ransomware Phobos. Opérant via un modèle de "Ransomware-as-a-Service" (RaaS), il gérait la distribution et la vente du logiciel malveillant auprès d'affiliés criminels depuis novembre 2020. Le gang a extorqué plus de 39 millions de dollars à plus de 1 000 organisations dans le monde, ciblant divers secteurs, dont la santé et l'éducation. Cette condamnation s'inscrit dans le cadre de l'opération internationale *Aether*, coordonnée par Europol, qui a permis de démanteler des infrastructures, d'arrêter plusieurs affiliés et de prévenir plus de 400 attaques.

**Points clés :**
*   **Modèle économique :** Les affiliés achetaient l'accès à Phobos et payaient environ 300 $ par déploiement pour obtenir une clé de déchiffrement, Ptitsyn percevant une part des rançons totales.
*   **Mode opératoire :** Utilisation intensive d'identifiants volés, exfiltration de données, chiffrement des systèmes et extorsion par menaces de divulgation publique des données volées.
*   **Action judiciaire :** Ptitsyn risque jusqu'à 20 ans de prison. L'opération *Aether* a permis de saisir de nombreux serveurs et de neutraliser des acteurs clés du réseau.

**Vulnérabilités :**
*   Le vecteur d'accès initial repose principalement sur l'utilisation d'identifiants compromis et l'exploitation de protocoles d'accès à distance (RDP) mal sécurisés, une faiblesse récurrente liée à la famille de ransomware Crysis dont Phobos est dérivé.

**Recommandations :**
*   **Sécurisation des accès :** Implémenter systématiquement l'authentification multifacteur (MFA) sur tous les accès distants et comptes à privilèges.
*   **Gestion des identifiants :** Surveiller les fuites d'identifiants et appliquer des politiques de mots de passe robustes pour prévenir les attaques par force brute.
*   **Sauvegardes :** Maintenir des sauvegardes hors ligne et immuables pour garantir la continuité d'activité en cas de chiffrement malveillant.
*   **Veille et surveillance :** Utiliser des solutions de détection d'anomalies sur le réseau pour identifier rapidement les mouvements latéraux caractéristiques des intrusions par ransomware.

---
[Source](https://www.bleepingcomputer.com/news/security/phobos-ransomware-admin-pleads-guilty-to-wire-fraud-conspiracy/){:target="_blank"}
