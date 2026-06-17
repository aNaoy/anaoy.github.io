---
title: 'FortiBleed leak exposes Fortinet VPN credentials for 73,000 devices.'
date: 2026-06-17
permalink: /posts/2026/06/17/fortibleed-leak-exposes-fortinet-vpn-credentials-for-73000-devices/
tags:
- veille-cyber
- bleepingcomp
---
### FortiBleed : Fuite massive d'identifiants VPN Fortinet

Une fuite de données majeure, baptisée "FortiBleed", a exposé les identifiants de connexion (noms d'utilisateur, e-mails et mots de passe en clair) de 73 932 appareils Fortinet/FortiGate à travers le monde. Cette base de données, découverte par le chercheur Bob Diachenko, contient des informations appartenant à de grandes entreprises (Samsung, Foxconn, Chevron, etc.), des agences gouvernementales et des opérateurs d'infrastructures critiques.

**Points clés :**
* **Ampleur :** Environ 75 000 appareils uniques sont impactés dans 194 pays.
* **Mode opératoire :** Un groupe cybercriminel russophone a orchestré une campagne massive de force brute (plus d'un milliard de tentatives) et intercepté des hashes d'authentification VPN, craqués via un cluster de GPU.
* **Origine des données :** Les analystes estiment que les données proviennent de fichiers de configuration exportés, permettant un accès administratif complet aux pare-feux.
* **Impact :** Les attaquants ont pu accéder aux environnements Active Directory internes et exfiltrer des documents sensibles.

**Vulnérabilités :**
* Aucune CVE spécifique n'est citée comme vecteur initial. La vulnérabilité réside principalement dans l'exposition directe des interfaces de gestion FortiGate sur Internet et l'exploitation de configurations exposées ou interceptées.

**Recommandations :**
* **Rotation immédiate :** Modifier tous les mots de passe associés aux accès VPN et aux interfaces d'administration Fortinet.
* **Authentification multifacteur (MFA) :** Activer systématiquement le MFA sur tous les accès distants et administratifs.
* **Audit de sécurité :** Examiner les journaux (logs) des passerelles à la recherche d'activités suspectes ou de mouvements latéraux.
* **Vérification :** Utiliser l'outil de recherche proposé par *Hudson Rock* pour vérifier si une organisation figure dans le jeu de données exposé.
* **Réduction de la surface d'attaque :** Restreindre l'accès aux interfaces d'administration des pare-feux pour qu'elles ne soient pas accessibles publiquement depuis Internet.

---
[Source](https://www.bleepingcomputer.com/news/security/fortibleed-leak-exposes-fortinet-vpn-credentials-for-73-000-devices/){:target="_blank"}
