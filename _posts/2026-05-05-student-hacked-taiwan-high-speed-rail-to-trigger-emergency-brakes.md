---
title: 'Student hacked Taiwan high-speed rail to trigger emergency brakes'
date: 2026-05-05
permalink: /posts/2026/05/05/student-hacked-taiwan-high-speed-rail-to-trigger-emergency-brakes/
tags:
- veille-cyber
- bleepingcomp
---
### Cyberattaque contre le réseau ferroviaire à grande vitesse de Taïwan

Un étudiant de 23 ans a été arrêté pour avoir paralysé le réseau ferroviaire à grande vitesse de Taïwan (THSR) le 5 avril dernier. En utilisant du matériel radio défini par logiciel (SDR) et des radios portatives, il a transmis un signal d'alarme prioritaire, provoquant l'arrêt d'urgence de quatre trains pendant 48 minutes. L'enquête a révélé la complicité d'un étudiant de 21 ans ayant fourni des paramètres techniques critiques.

**Points clés :**
*   **Méthode :** Interception et décodage des paramètres du protocole TETRA (Trans-European Trunked Radio) via SDR, suivis d'un clonage d'identifiants légitimes.
*   **Impact :** Immobilisation de quatre trains et interruption du service pendant près d'une heure.
*   **Détection :** Analyse des logs du réseau TETRA identifiant une balise non assignée, couplée à l'exploitation des caméras de surveillance.
*   **Responsabilité :** Négligence systémique, le protocole TETRA utilisé n'ayant pas été mis à jour (rotation des clés) depuis 19 ans.

**Vulnérabilités :**
*   **Absence de rotation des clés :** La non-actualisation des paramètres de sécurité pendant 19 ans a permis le contournement de sept couches de vérification.
*   **Clonage d'identité :** Absence de mécanismes robustes pour authentifier les terminaux radio au sein du réseau, permettant l'usurpation de balises autorisées.
*(Note : Aucune CVE spécifique n'est associée à cet incident, car il s'agit d'une faille de configuration et de gestion de cycle de vie des systèmes de communication).*

**Recommandations :**
*   **Rotation régulière des clés :** Appliquer une politique stricte de renouvellement des paramètres de chiffrement et d'authentification pour les systèmes hérités.
*   **Renforcement de l'authentification :** Implémenter des mécanismes d'authentification mutuelle plus robustes pour prévenir le clonage de terminaux.
*   **Audit et surveillance :** Mettre en place une surveillance en temps réel du trafic réseau pour détecter toute anomalie ou activité provenant de terminaux non répertoriés ou non autorisés.

---
[Source](https://www.bleepingcomputer.com/news/security/student-hacked-taiwan-high-speed-rail-to-trigger-emergency-brakes/){:target="_blank"}
