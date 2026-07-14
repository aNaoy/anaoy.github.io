---
title: '148 npm Packages Disguised as Student Proxies Turned Browsers Into a DDoS Botnet'
date: 2026-07-14
permalink: /posts/2026/07/14/148-npm-packages-disguised-as-student-proxies-turned-browsers-into-a-ddos-botnet/
tags:
- veille-cyber
- hackernews
---
### Botnet par procuration : 148 paquets npm détournés

Une campagne malveillante a utilisé 148 paquets npm, déguisés en outils de contournement de filtres web pour étudiants (proxy), pour transformer les navigateurs des utilisateurs en un botnet DDoS sans le moindre script d'installation.

**Points clés :**
*   **Mode opératoire :** Les paquets ne visent pas les développeurs, mais les étudiants utilisant ces sites de proxy « Lucide ». Le code malveillant s'exécute directement dans le navigateur de la victime.
*   **Mécanismes d'attaque :**
    *   **G2 (Remote Loader) :** Télécharge dynamiquement du code JavaScript non vérifié (via jsDelivr) et l'exécute avec les privilèges complets de l'origine (accès aux cookies et au stockage local).
    *   **HTTP Flood :** Génère des requêtes POST massives vers des cibles spécifiques (ex: un domaine académique).
    *   **Wisp Attack :** Utilise le protocole Wisp pour saturer les serveurs proxy tiers par une avalanche de requêtes WebSocket, provoquant une épuisement des descripteurs de fichiers et des logs.
*   **Persistance :** Le code est conçu pour être « réactivable » à distance. Bien que les fonctions DDoS aient été temporairement désactivées, les attaquants peuvent réinjecter la charge utile via une simple mise à jour sur leur dépôt GitHub sans modifier le paquet npm.

**Vulnérabilités exploitées :**
*   **Absence de contrôle d'intégrité :** Utilisation de branches GitHub mutables sans vérification d'intégrité des sous-ressources (SRI).
*   **Abus de protocole :** Exploitation du protocole Wisp (`wisp-server-node`) qui ne vérifie pas la destination des connexions, permettant de saturer les ressources du serveur.

**Recommandations :**
*   **Blocage réseau :** Filtrer au niveau DNS les domaines associés à la campagne (notamment `woofbeginner[.]com` et `c.vipersfutbol[.]com`).
*   **Nettoyage local :** Pour les utilisateurs ayant visité ces sites, effacer le cache du navigateur, le stockage local et supprimer les *Service Workers* suspects.
*   **Hygiène logicielle :** Supprimer immédiatement ces paquets des fichiers de dépendances (`package-lock.json`, `manifests`) et effectuer une reconstruction propre de l'environnement de développement.
*   **Vigilance :** Ne pas se reposer uniquement sur les scanners de dépendances traditionnels, car ce type de menace ne s'exécute pas lors de l'installation, mais lors de l'utilisation du service web.

---
[Source](https://thehackernews.com/2026/07/148-npm-packages-disguised-as-student.html){:target="_blank"}
