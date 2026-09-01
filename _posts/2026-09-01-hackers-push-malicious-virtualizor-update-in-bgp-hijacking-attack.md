---
title: 'Hackers push malicious Virtualizor update in BGP hijacking attack'
date: 2026-09-01
permalink: /posts/2026/09/01/hackers-push-malicious-virtualizor-update-in-bgp-hijacking-attack/
tags:
- veille-cyber
- bleepingcomp
---
### Attaque par détournement BGP sur l'infrastructure Virtualizor

Entre le 28 et le 30 août, les serveurs de mise à jour de la solution de gestion VPS *Virtualizor* (Softaculous) ont été la cible d'une attaque par détournement de protocole BGP (*Border Gateway Protocol*). En usurpant les routes IP, les attaquants ont intercepté les requêtes des serveurs clients pour leur délivrer une mise à jour malveillante.

**Points clés :**
*   **Méthode :** Détournement BGP ayant permis de rediriger le trafic légitime vers des serveurs contrôlés par les attaquants.
*   **Impact :** Un nombre limité d'installations Virtualizor a reçu un package de mise à jour corrompu. Les informations d'accès au portail client/facturation ont également pu être compromises.
*   **Réponse :** Softaculous a restauré le routage, révoqué les certificats frauduleux et publié la version 3.2.9.9 incluant un nouvel outil « Security Analyzer ».

**Vulnérabilités :**
*   Aucune CVE spécifique n'a été attribuée, l'incident reposant sur une faille structurelle du protocole réseau (BGP) et sur l'absence de signature cryptographique des paquets de mise à jour au moment des faits.

**Recommandations pour les administrateurs :**
*   **Audit immédiat :** Rechercher sur les serveurs la présence d'un service nommé `virt_check`.
*   **Remédiation système :** En cas de compromission, révoquer et renouveler toutes les clés d'API. Rechercher des accès non autorisés (clés SSH), des comptes créés, des tâches planifiées suspectes ou des connexions sortantes inhabituelles.
*   **Sécurité des comptes :** Réinitialiser les mots de passe du portail client Softaculous et surveiller les relevés bancaires pour toute activité suspecte si des informations de paiement ont été saisies durant la période de l'incident.
*   **Mise à jour :** Installer la version 3.2.9.9 et utiliser le nouvel outil d'analyse de sécurité intégré.
*   **Futur :** Softaculous prévoit l'implémentation obligatoire de la signature cryptographique pour tous les futurs paquets logiciels.

---
[Source](https://www.bleepingcomputer.com/news/security/hackers-push-malicious-virtualizor-update-in-bgp-hijacking-attack/){:target="_blank"}
