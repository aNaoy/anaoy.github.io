---
title: 'Surge in coordinated scans targets Microsoft RDP auth servers'
date: 2025-08-26
permalink: /posts/2025/08/26/surge-in-coordinated-scans-targets-microsoft-rdp-auth-servers/
tags:
- veille-cyber
- bleepingcomp
---
**Détection de Balayages Coordonnés des Portails d'Authentification RDP Microsoft**

Une augmentation significative de l'activité de balayage ciblant les portails d'authentification Microsoft Remote Desktop Web Access et RDP Web Client a été observée. Près de 2 000 adresses IP ont participé à cette campagne de reconnaissance coordonnée, contrastant fortement avec les 3 à 5 adresses IP habituelles.

**Points Clés :**

*   **Objectif :** Les balayages visent à identifier des vulnérabilités de synchronisation exploitables pour vérifier des noms d'utilisateur, préparant ainsi des attaques basées sur les identifiants comme le bourrage d'identifiants ou le "password spraying".
*   **Mécanisme :** Les vulnérabilités de synchronisation exploitent les différences subtiles dans les temps de réponse du système entre les tentatives de connexion avec un utilisateur valide et invalide pour déduire la validité d'un nom d'utilisateur.
*   **Origine et Ciblage :** Une grande majorité des adresses IP (92% de celles identifiées par une signature client commune) ont été précédemment signalées comme malveillantes, avec une prédominance d'origines brésiliennes ciblant des adresses IP aux États-Unis, suggérant potentiellement un outil unique ou un botnet.
*   **Contexte Temporel :** Le moment de cette vague de balayages coïncide avec la rentrée scolaire aux États-Unis, une période où les établissements d'enseignement réactivent leurs systèmes RDP et intègrent de nouveaux comptes, souvent avec des formats de nom d'utilisateur prévisibles.
*   **Corrélation avec les Vulnérabilités :** L'augmentation de ce trafic malveillant pourrait également indiquer la découverte d'une nouvelle faille de sécurité, car des pics d'activité de ce type précèdent fréquemment la divulgation de nouvelles vulnérabilités.

**Vulnérabilités Mentionnées :**

*   Vulnérabilités de synchronisation dans les processus d'authentification RDP permettant la découverte de noms d'utilisateur. (Aucun CVE spécifique n'est mentionné dans l'article pour cette activité particulière.)

**Recommandations :**

*   Les administrateurs gérant les portails RDP et les appareils exposés doivent s'assurer que leurs comptes sont sécurisés avec une authentification multifacteur.
*   Si possible, il est recommandé de placer ces portails derrière des VPN.

---
[Source](https://www.bleepingcomputer.com/news/security/surge-in-coordinated-scans-targets-microsoft-rdp-auth-servers/){:target="_blank"}
