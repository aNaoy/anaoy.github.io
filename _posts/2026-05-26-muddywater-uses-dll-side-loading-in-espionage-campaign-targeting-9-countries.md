---
title: 'MuddyWater Uses DLL Side-Loading in Espionage Campaign Targeting 9 Countries'
date: 2026-05-26
permalink: /posts/2026/05/26/muddywater-uses-dll-side-loading-in-espionage-campaign-targeting-9-countries/
tags:
- veille-cyber
- hackernews
---
### Campagne d'espionnage MuddyWater : Tactiques de DLL Side-Loading et vol de données

Le groupe de hackers iranien MuddyWater a lancé une vaste campagne d'espionnage au premier trimestre 2026, ciblant des secteurs critiques (industrie, éducation, finances, services publics) dans neuf pays. Cette opération se distingue par une montée en compétence dans l'hygiène opérationnelle, privilégiant la discrétion et l'utilisation d'outils légitimes pour masquer ses activités malveillantes.

**Points clés :**
*   **Technique principale :** Utilisation du *DLL side-loading* pour charger des DLL malveillantes via des exécutables signés (Fortemedia et SentinelOne).
*   **Vol de données :** Utilisation de l'outil *ChromElevator* pour contourner le chiffrement App-Bound Encryption (ABE) des navigateurs Chromium et exfiltrer mots de passe et cookies.
*   **Persistance et mouvement :** Utilisation de scripts Node.js pour déployer des charges utiles PowerShell, effectuer des reconnaissances (capture d'écran, vol de jetons SAM) et établir des tunnels SOCKS5.
*   **Exfiltration :** Les données volées sont parfois temporairement stockées sur des services publics comme `sendit.sh`.
*   **Évolution :** Le groupe délaisse les opérations bruyantes pour des méthodes plus disciplinées, visant l'implantation durable plutôt qu'une présence continue.

**Vulnérabilités exploitées :**
*   **DLL Side-Loading :** Abus des binaires `fmapp.exe` et `sentinelmemoryscanner.exe` pour exécuter des DLL malveillantes (`fmapp.dll`, `sentinelagentcore.dll`).
*   **ChromElevator :** Exploitation spécifique visant le contournement de l'App-Bound Encryption (ABE) dans les navigateurs basés sur Chromium.
*   **Outils légitimes :** Utilisation de `proxychains`, `Node.js` et divers services de transfert de fichiers légitimes pour dissimuler le trafic C2 (Command & Control).

**Recommandations de sécurité :**
*   **Surveillance des binaires :** Auditer les répertoires d'applications pour détecter la présence de fichiers DLL suspects à côté d'exécutables légitimes signés.
*   **Protection des navigateurs :** Renforcer les politiques de sécurité autour des données des navigateurs (mots de passe, cookies) et restreindre l'exécution de scripts tiers capables d'accéder aux répertoires de profils utilisateurs.
*   **Détection comportementale :** Surveiller l'utilisation inhabituelle de PowerShell, notamment lorsqu'il est appelé par des processus non-système (comme `node.exe` ou des binaires tiers).
*   **Filtrage réseau :** Bloquer les connexions sortantes vers des services de partage de fichiers non approuvés par l'entreprise et restreindre les tunnels SOCKS5 non autorisés au sein du périmètre réseau.
*   **Gestion des accès :** Surveiller étroitement le vidage des identifiants (Credential Dumping) et les tentatives d'accès aux fichiers sensibles (SAM hive) pour prévenir les mouvements latéraux.

---
[Source](https://thehackernews.com/2026/05/muddywater-uses-dll-side-loading-in.html){:target="_blank"}
