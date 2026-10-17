---
title: 'MALFEX npm Package imgdecode Hides Shellcode Loader in Windows Native Addon'
date: 2026-10-17
permalink: /posts/2026/10/17/malfex-npm-package-imgdecode-hides-shellcode-loader-in-windows-native-addon/
tags:
- veille-cyber
- hackernews
---
### Campagne MALFEX : Menace persistante via des paquets npm malveillants

La campagne MALFEX, active depuis août 2023, exploite la supply chain du gestionnaire de paquets npm pour compromettre les systèmes Windows. L'attaquant publie continuellement des paquets malveillants, remplaçant rapidement ceux supprimés par les modérateurs, afin de déployer des logiciels espions (stealers) et des outils d'accès à distance (RAT).

**Points clés :**
*   **Mode opératoire :** Le paquet récent `imgdecode` utilise un add-on natif Node.js (DLL) pour charger du shellcode. Ce code est récupéré via GitHub, déchiffré en mémoire, puis injecté dans le processus `dllhost.exe`.
*   **Persistance et évasion :** Le malware intègre des capacités d'anti-analyse (détection de VMs/sandboxes), assure sa persistance via des clés de registre et des tâches planifiées (« MicrosoftEdgeUpdateService »), et communique avec un serveur C2 via WebSocket.
*   **Objectifs :** Vol de données sensibles (fichiers .pem, .kdbx, portefeuilles crypto, sessions de messageries comme Discord/Telegram) et prise de contrôle totale de la machine (exécution de commandes, captures d'écran, keylogging).
*   **Réactivité de l'attaquant :** L'acteur derrière MALFEX adapte ses techniques en temps réel, remplaçant les paquets détectés (ex: `native-runner`, `img-to-native`) par de nouvelles itérations (`runhelper`, `imgdecode`, `imgbundle`) en quelques jours.

**Vulnérabilités :**
Aucun identifiant CVE n'est associé à cette campagne, car il s'agit d'une attaque par **empoisonnement de dépendances (supply chain attack)** utilisant du code malveillant intégré volontairement dans des paquets légitimes en apparence.

**Recommandations :**
*   **Audit immédiat :** Si vous avez utilisé des paquets suspects (`imgdecode`, `imgbundle`, `native-runner`, `cdn-img-fetch`, `runhelper`, `img-to-native`), considérez la machine comme compromise.
*   **Isolation et nettoyage :** Isolez les systèmes infectés du réseau. Recherchez et supprimez la tâche planifiée suspecte « MicrosoftEdgeUpdateService » et les clés de registre associées.
*   **Rotation des accès :** Réinitialisez tous les mots de passe, clés SSH/API, et transférez les actifs numériques (cryptomonnaies) vers des portefeuilles sécurisés, car les données locales ont été exposées.
*   **Sécurisation :** Analysez systématiquement les dépendances tierces avant leur intégration et restreignez l'accès aux registres publics dans les environnements de build.

---
[Source](https://thehackernews.com/2026/10/malfex-npm-package-imgdecode-hides.html){:target="_blank"}
