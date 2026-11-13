---
title: 'SilentAir Hijacks Asian Telecom Networks to Intercept SMS 2FA Codes and Spy on Taiwanese Users'
date: 2026-11-13
permalink: /posts/2026/11/13/silentair-hijacks-asian-telecom-networks-to-intercept-sms-2fa-codes-and-spy-on-taiwanese-users/
tags:
- veille-cyber
- hackernews
---
### SilentAir : Piratage des réseaux télécoms asiatiques pour l'interception de communications

Le groupe d'espionnage **SilentAir** a compromis des équipements au sein d'opérateurs mobiles en Asie pour intercepter des SMS et des appels, ciblant principalement des personnalités politiques et gouvernementales à Taïwan. L'acteur, vraisemblablement étatique, exploite la confiance accordée au réseau d'interconnexion **IPX** pour détourner les communications.

#### Points clés
*   **Mode opératoire :** Les attaquants utilisent des équipements piratés au sein des réseaux opérateurs pour envoyer des messages de signalisation (**SS7** et **Diameter**) de type *UpdateLocation*. Cela leur permet de faire croire au réseau de l'abonné victime que leur équipement gère désormais sa ligne, redirigeant ainsi ses SMS et appels.
*   **Interception :** L'objectif principal semble être l'interception de codes de double authentification (2FA) pour compromettre des comptes tiers.
*   **SMS silencieux :** Utilisation massive de "SMS silencieux" (non affichés à l'utilisateur) pour vérifier l'efficacité des détournements, souvent camouflés en spams anodins.
*   **Attribution :** Des indices pointent vers un acteur opérant sur le fuseau horaire UTC+8, avec une activité synchronisée sur les jours ouvrés chinois, suggérant une origine potentielle liée à la Chine.

#### Vulnérabilités
L'attaque repose sur la confiance inhérente aux protocoles de signalisation télécoms hérités (**SS7** et **Diameter**) et sur le manque de segmentation au sein des réseaux d'interconnexion **IPX**. Aucune CVE spécifique n'est mentionnée, car il s'agit d'une exploitation de la logique des protocoles et d'une compromission physique/logicielle des équipements réseau (utilisant potentiellement des outils comme *SIGweaver* ou des variantes de malwares type *GTPDoor*).

#### Recommandations pour les opérateurs
*   **Sécurité périmétrique :** Déployer et interconnecter des pare-feu **GTP-C** et **GTP-U** avec les solutions de protection SS7/Diameter.
*   **Architecture "Zero Trust" :** Considérer l'ensemble du réseau IPX comme non fiable.
*   **Détection interne :** Mettre en place des mécanismes de surveillance des protocoles de signalisation à l'intérieur du réseau propre.
*   **Convergence IT/Télécom :** Intégrer la sécurité de la signalisation à la stratégie globale de cybersécurité IT de l'entreprise.

---
[Source](https://thehackernews.com/2026/11/silentair-hijacks-asian-telecom.html){:target="_blank"}
