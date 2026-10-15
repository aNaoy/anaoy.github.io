---
title: 'YuanKong RAT: the Android remote-control service that stamps its operators names into every build'
date: 2026-10-15
permalink: /posts/2026/10/15/yuankong-rat-the-android-remote-control-service-that-stamps-its-operators-names-into-every-build/
tags:
- veille-cyber
- zerodaysfans
---
### Analyse du Trojan d'accès à distance YuanKong sur Android

YuanKong est une famille de malwares Android multi-locataires utilisant une architecture de "dropper" (chargeur) simple qui installe un RAT (Remote Access Tool) de contrôle à distance. Chaque build est personnalisée par des identifiants d'opérateur codés en dur, permettant de lier chaque infection à un compte spécifique sur le panneau de contrôle.

**Points clés :**
*   **Architecture :** Le dropper contient un fichier `vault-config.json` en clair, révélant la clé et l'IV nécessaires pour déchiffrer la charge utile (chiffrement faible par double XOR "SVLT-XOR-v2").
*   **Multi-tenant :** Chaque build est configuré avec un `apkAccountId` et un `apkAccountName` uniques. Ces données sont rapportées au serveur C2, permettant d'identifier l'opérateur derrière chaque échantillon.
*   **Persistance et Escalade :** Le malware utilise l'accessibilité Android pour activer le "Débogage sans fil", s'appaire localement à `adbd` (via SPAKE2), et s'octroie des permissions système (ex: `WRITE_SECURE_SETTINGS`) pour installer un daemon persistant impossible à tuer.
*   **Capacités :** Capture d'écran, enregistrement des frappes clavier, détournement du presse-papier, lecture des notifications (OTP) et overlay phishing pour voler des codes PIN bancaires.

**Vulnérabilités exploitées :**
*   **Abus de l'API d'Accessibilité :** Utilisée pour automatiser les interactions utilisateur, capturer des données sensibles et manipuler les paramètres système.
*   **Détournement de l'ADB local :** L'application utilise une bibliothèque pour se connecter au daemon ADB du téléphone lui-même, contournant ainsi le bac à sable (sandbox) Android pour obtenir des privilèges `shell` (uid 2000).

**Recommandations :**
*   **Blocage réseau :** Bloquer les domaines `apppanda[.]xyz`, `ktxapp[.]com`, `ktx123[.]net` et l'adresse IP `206.82.1.14`.
*   **Détection par signature :** Utiliser l'empreinte SHA-256 du certificat de signature du RAT (et non du dropper) pour la détection : `73cbe8e3730cacfdd208f22eab468bb5495a78c0eb2cb37eff5af0cafe321387`.
*   **Surveillance système :** Surveiller l'activation inattendue du "Débogage sans fil" dans les paramètres système et l'octroi suspect de permissions via `pm grant` par des applications tierces.
*   **Politique de sécurité :** Restreindre l'utilisation des services d'accessibilité aux applications légitimes et de confiance sur les parcs d'appareils gérés.

---
[Source](https://starlabs.sg/blog/2026/10-yuankong-rat-the-android-remote-control-service-that-stamps-its-operators-names-into-every-build/){:target="_blank"}
