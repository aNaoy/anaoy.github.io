---
title: 'CERT Polska Details Coordinated Cyber Attacks on 30+ Wind and Solar Farms'
date: 2026-01-31
permalink: /posts/2026/01/31/cert-polska-details-coordinated-cyber-attacks-on-30-wind-and-solar-farms/
tags:
- veille-cyber
- hackernews
---
### Cyberattaques Coordonnées Contre des Infrastructures Énergétiques et Industrielles

Des attaques informatiques coordonnées ont visé plus de 30 parcs éoliens et solaires, une entreprise manufacturière et une centrale de cogénération en Pologne le 29 décembre 2025. Ces attaques, attribuées au groupe "Static Tundra" (également connu sous de nombreux autres noms et potentiellement lié au FSB russe), avaient un objectif purement destructeur.

Bien que les attaques contre les fermes d'énergies renouvelables aient perturbé les communications, elles n'ont pas affecté la production d'électricité. L'attaque contre la centrale de cogénération n'a pas non plus réussi à interrompre l'approvisionnement en chaleur. Cependant, des activités de vol de données à long terme ont été observées dans ce dernier cas.

Dans le secteur manufacturier, l'accès initial semble avoir été opportuniste, exploité via un appareil de périmètre Fortinet vulnérable. Des vulnérabilités similaires sur des appareils FortiGate ont également été impliquées dans une attaque visant un point de connexion au réseau électrique.

Les attaquants ont cherché à accéder aux réseaux internes, à endommager le micrologiciel des contrôleurs, à supprimer des fichiers système et à déployer des malwares destructeurs. Deux malwares spécifiques ont été identifiés :

*   **DynoWiper** : Déployé sur des ordinateurs HMI (Human-Machine Interface) et des partages réseau, il utilise le générateur de nombres aléatoires Mersenne Twister pour corrompre et supprimer des fichiers. Son déploiement s'est fait via un accès au portail SSL-VPN d'un FortiGate, en utilisant des identifiants statiques et sans authentification à deux facteurs.
*   **LazyWiper** : Détecté dans le secteur manufacturier, ce malware basé sur PowerShell écrase les fichiers avec des séquences pseudo-aléatoires. Il est suspecté d'avoir été développé à l'aide d'un grand modèle linguistique.

Dans le cas de la centrale de cogénération et de l'entreprise manufacturière, les malwares ont été distribués au sein du domaine Active Directory via des scripts PowerShell exécutés sur un contrôleur de domaine.

Les attaquants ont également tenté d'accéder à des services cloud (M365) en utilisant des identifiants obtenus localement, téléchargeant des données relatives à la modernisation des réseaux OT, aux systèmes SCADA et aux travaux techniques.

**Points Clés:**

*   Attaques coordonnées visant des infrastructures critiques et industrielles.
*   Objectif principal : destruction et perturbation.
*   Utilisation de malwares destructeurs (wipers) : DynoWiper et LazyWiper.
*   Exploitation de vulnérabilités sur des équipements Fortinet/FortiGate.
*   Tentatives de vol de données et d'accès aux services cloud.
*   Utilisation d'identifiants statiques et absence de MFA comme vecteurs d'accès.

**Vulnérabilités (CVE non spécifiées dans l'article, mais des types sont mentionnés):**

*   Appareils de périmètre Fortinet vulnérables.
*   Appareils FortiGate vulnérables (exploitation via le portail SSL-VPN).
*   Faiblesses dans la gestion des identifiants (identifiants statiques, absence d'authentification à deux facteurs).

**Recommandations (implicites et explicites dans l'article):**

*   Sécuriser les équipements de périmètre, y compris les appareils Fortinet/FortiGate, en les maintenant à jour et en les configurant correctement.
*   Mettre en œuvre une authentification forte, notamment l'authentification multifacteur (MFA), pour tous les accès, y compris pour les comptes statiques.
*   Surveiller activement les réseaux pour détecter les activités suspectes, notamment les mouvements latéraux et les tentatives d'accès aux données sensibles.
*   Sécuriser la gestion des identifiants et éviter les configurations avec des identifiants statiques.
*   Renforcer la sécurité des systèmes SCADA et des environnements OT.
*   Mettre en place des plans de réponse aux incidents robustes pour faire face à de telles attaques.

---
[Source](https://thehackernews.com/2026/01/poland-attributes-december-cyber.html){:target="_blank"}
