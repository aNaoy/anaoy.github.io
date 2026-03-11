---
title: 'Iran-Backed Hackers Claim Wiper Attack on Medtech Firm Stryker'
date: 2026-03-11
permalink: /posts/2026/03/11/iran-backed-hackers-claim-wiper-attack-on-medtech-firm-stryker/
tags:
- veille-cyber
- krebs
---
### Cyberattaque dévastatrice contre le géant médical Stryker

Le groupe de hacktivistes **Handala**, affilié au ministère iranien du Renseignement (MOIS), a revendiqué une attaque massive par effacement de données (wiper) contre l’entreprise de technologie médicale Stryker. L'incident a paralysé les opérations mondiales de la société, entraînant la fermeture de bureaux et forçant des milliers d'employés à cesser leurs activités.

**Points clés :**
*   **Mode opératoire :** Contrairement à un logiciel malveillant classique, les assaillants auraient détourné l'outil d'administration cloud **Microsoft Intune** pour envoyer une commande de réinitialisation à distance ("remote wipe") sur l'ensemble des systèmes, serveurs et appareils mobiles connectés.
*   **Revendication :** L'attaque est présentée par Handala comme des représailles à une frappe de missile américaine ayant touché une école en Iran.
*   **Impact opérationnel :** Plus de 200 000 systèmes ont été effacés. Des sites à travers 79 pays sont touchés, perturbant potentiellement la chaîne d'approvisionnement des hôpitaux américains qui dépendent des équipements de Stryker.
*   **Acteur de la menace :** Handala est considéré comme un alias opérationnel du groupe **Void Manticore**, spécialisé dans les attaques opportunistes et le piratage psychologique.

**Vulnérabilités :**
*   Aucune CVE spécifique n'est mentionnée, car l'attaque exploite une fonctionnalité légitime (l'administration via Microsoft Intune) plutôt qu'une faille logicielle. Il s'agit d'un détournement de privilèges administratifs au sein d'une infrastructure de gestion centralisée.

**Recommandations :**
*   **Sécurisation des accès :** Appliquer une authentification multifacteur (MFA) renforcée et des politiques d'accès conditionnel strictes sur les plateformes de gestion d'appareils (MDM) telles que Microsoft Intune.
*   **Gestion des privilèges :** Restreindre rigoureusement le nombre d'administrateurs ayant le pouvoir d'émettre des commandes globales de réinitialisation ("wipe") sur le parc informatique.
*   **Monitoring :** Surveiller les alertes de connexion inhabituelles sur les consoles d'administration cloud et mettre en place des alertes spécifiques en cas d'exécution de commandes de réinitialisation de masse.
*   **Continuité :** En cas de compromission, isoler immédiatement les comptes administrateurs touchés et évaluer la nécessité de désactiver temporairement les agents de gestion à distance pour stopper la propagation de l'effacement.

---
[Source](https://krebsonsecurity.com/2026/03/iran-backed-hackers-claim-wiper-attack-on-medtech-firm-stryker/){:target="_blank"}
