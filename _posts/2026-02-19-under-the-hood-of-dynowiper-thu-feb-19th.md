---
title: 'Under the Hood of DynoWiper, (Thu, Feb 19th)'
date: 2026-02-19
permalink: /posts/2026/02/19/under-the-hood-of-dynowiper-thu-feb-19th/
tags:
- veille-cyber
- sans-isc
---
### DynoWiper : Analyse d'un logiciel destructeur de données

Ce logiciel malveillant, nommé DynoWiper, a été identifié lors d'attaques contre des entreprises du secteur énergétique polonais fin décembre 2025. Son architecture et ses méthodes d'exécution le lient à des acteurs étatiques russes, potentiellement le groupe APT Sandworm, connu pour ses opérations contre l'Ukraine.

**Points Clés :**

*   **Type de Malware :** Logiciel destructeur de données (wiper).
*   **Cible :** Environnements Windows (version analysée : 32 bits).
*   **Fonctionnement Principal :**
    *   Initialisation d'un générateur de nombres pseudo-aléatoires (Mersenne Twister MT19937) avec une valeur de départ fixe puis aléatoire.
    *   Parcours des lecteurs et des répertoires (en excluant des répertoires système critiques).
    *   Corruptions de fichiers par l'écriture répétée de 16 octets de données aléatoires à des positions sélectionnées.
    *   Suppression des fichiers corrompus.
    *   Activation du privilège `SeShutdownPrivilege` pour forcer un redémarrage du système.

**Vulnérabilités exploitées / Techniques utilisées (correspondance MITRE ATT&CK) :**

*   **T1680: Local Storage Discovery** (Découverte du stockage local)
*   **T1083: File and Directory Discovery** (Découverte de fichiers et répertoires)
*   **T1222.001: Windows File and Directory Permissions Modification** (Modification des permissions de fichiers et répertoires Windows)
*   **T1134: Access Token Manipulation** (Manipulation du jeton d'accès) - Utilisé pour l'évasion de défense et l'escalade de privilèges.
*   **T1485: Data Destruction** (Destruction de données)
*   **T1529: System Shutdown/Reboot** (Arrêt/Redémarrage du système)

**Recommandations (implicites par l'analyse) :**

Bien que l'article ne détaille pas de recommandations spécifiques, une analyse de ce type suggère la nécessité des mesures suivantes :

*   **Détection et prévention :** Mettre en place des solutions de sécurité capables de détecter et bloquer les fichiers exécutables inconnus et suspects, ainsi que les comportements anormaux d'écriture et de suppression de fichiers.
*   **Gestion des accès et privilèges :** Appliquer le principe du moindre privilège pour limiter l'impact potentiel d'un compte compromis.
*   **Sauvegardes régulières :** Disposer de sauvegardes récentes et vérifiées est essentiel pour pouvoir restaurer les données en cas d'incident.
*   **Surveillance des systèmes :** Surveiller les journaux d'événements et l'activité réseau pour détecter des signes d'intrusion et de corruption de données.
*   **Mises à jour et patchs :** Maintenir les systèmes d'exploitation et les logiciels à jour pour corriger d'éventuelles vulnérabilités.

---
[Source](https://isc.sans.edu/diary/rss/32730){:target="_blank"}
