---
title: 'FortiBleed leak exposes Fortinet VPN credentials for 73,000 devices.'
date: 2026-06-18
permalink: /posts/2026/06/18/fortibleed-leak-exposes-fortinet-vpn-credentials-for-73000-devices/
tags:
- veille-cyber
- bleepingcomp
---
### FortiBleed : Fuite massive d'identifiants Fortinet

Une faille de sécurité majeure, baptisée « FortiBleed », a exposé les identifiants de connexion de près de 74 000 équipements VPN Fortinet et pare-feux FortiGate à travers le monde. Cette base de données, découverte par le chercheur Bob Diachenko, contient des informations sensibles (noms d'utilisateurs, emails et mots de passe en clair) utilisées par des entreprises multinationales et des agences gouvernementales.

**Points clés :**
* **Étendue de la compromission :** 73 932 instances VPN/pare-feux concernées dans 194 pays, incluant des secteurs critiques (finance, santé, défense, télécommunications).
* **Mode opératoire :** Un groupe cybercriminel russophone a orchestré une campagne massive de force brute (plus d'un milliard de tentatives). Les attaquants ont intercepté des hashs d'authentification SSL VPN, les ont cassés via un cluster de GPU, puis ont utilisé ces accès pour se déplacer latéralement dans les réseaux internes (Active Directory).
* **Origine probable :** Les données proviendraient de fichiers de configuration exportés de FortiGate, suggérant une compromission directe des systèmes plutôt qu'une simple faille logicielle isolée.
* **Vulnérabilité :** Aucune CVE spécifique n'a été identifiée comme vecteur d'entrée initial ; l'exposition semble résulter d'une mauvaise gestion des interfaces d'administration exposées sur Internet et de méthodes d'extraction de configuration encore non élucidées.

**Recommandations immédiates :**
1. **Réinitialisation des accès :** Modifier immédiatement tous les mots de passe associés aux interfaces d'administration et aux accès VPN Fortinet.
2. **Renforcement de l'authentification :** Imposer l'authentification multifacteur (MFA) sur tous les accès distants et administratifs.
3. **Audit de sécurité :** Examiner les journaux (logs) des passerelles à la recherche d'activités suspectes ou de connexions non autorisées.
4. **Vérification :** Utiliser les outils de recherche disponibles (comme celui proposé par *Hudson Rock*) pour vérifier si une organisation est présente dans le jeu de données exposé.
5. **Réduction de la surface d'attaque :** Limiter l'exposition des interfaces d'administration FortiGate directement sur Internet.

---
[Source](https://www.bleepingcomputer.com/news/security/fortibleed-leak-exposes-fortinet-vpn-credentials-for-73-000-devices/){:target="_blank"}
