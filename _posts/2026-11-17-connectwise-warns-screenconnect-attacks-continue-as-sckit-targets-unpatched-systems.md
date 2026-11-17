---
title: 'ConnectWise Warns ScreenConnect Attacks Continue as SCKit Targets Unpatched Systems'
date: 2026-11-17
permalink: /posts/2026/11/17/connectwise-warns-screenconnect-attacks-continue-as-sckit-targets-unpatched-systems/
tags:
- veille-cyber
- hackernews
---
### Menace persistante contre ScreenConnect : Le malware SCKit

ConnectWise a confirmé la persistance d'attaques visant ses environnements ScreenConnect. Les acteurs malveillants exploitent des vulnérabilités critiques pour déployer le toolkit **SCKit**, capable de se propager comme un ver de l'appareil infecté vers la machine du technicien informatique. Ce malware utilise des extensions tierces compromises pour contourner les contrôles d'authentification et établir une persistance, notamment en se faisant passer pour le service « Windows Update Agent ».

**Points clés :**
*   **Propagation latérale :** Le malware cible les techniciens MSP lors de leurs sessions de support à distance.
*   **Infrastructure malveillante :** Utilisation d'un hébergeur « bulletproof » (1337 Services GmbH) pour diffuser des clients ScreenConnect corrompus.
*   **Action immédiate de l'éditeur :** ConnectWise a désactivé de manière préventive cinq extensions tierces (notamment RMM+ et Labtech Plus) sur plus de 400 environnements partenaires.

**Vulnérabilités :**
*   **CVE-2026-84869 (Score CVSS 9.9) :** Permet le transfert et l'exécution non autorisés de fichiers lors d'une session distante active.
*   **Défauts d'authentification :** Vulnérabilités dans les versions 1.0.31 et 1.0.32 de RMM+ permettant l'exécution de commandes non autorisées.

**Recommandations :**
*   **Mise à jour immédiate :** Passer impérativement à la version 26.6.5 ou supérieure du client ScreenConnect.
*   **Gestion des extensions :** Ne pas réactiver ni réinstaller les extensions tierces identifiées par ConnectWise avant instruction contraire.
*   **Audit de sécurité :** La mise à jour et la désactivation des extensions ne suffisant pas à supprimer une persistance déjà établie, il est crucial d'auditer les systèmes compromis pour détecter tout processus malveillant (comme `UpdateConnect.ClientService.exe`) ou accès non autorisé.

---
[Source](https://thehackernews.com/2026/11/connectwise-warns-screenconnect-attacks.html){:target="_blank"}
