---
title: 'Operation QUICSILVER Targets Myanmar Government and IT with QUICAgent Backdoor'
date: 2026-08-24
permalink: /posts/2026/08/24/operation-quicsilver-targets-myanmar-government-and-it-with-quicagent-backdoor/
tags:
- veille-cyber
- hackernews
---
### Opération QUICSILVER : Espionnage ciblé au Myanmar via QUICAgent

La campagne d'espionnage cybernétique « Opération QUICSILVER », attribuée avec une confiance modérée à un acteur lié à la Chine, cible les secteurs gouvernementaux et informatiques au Myanmar. Elle repose sur l'utilisation de leurres (invitations à des cérémonies de remise de diplômes ou calendriers officiels) pour déployer une porte dérobée nommée **QUICAgent**.

**Points clés :**
*   **Vecteur d'infection :** Fichiers VHD contenant des raccourcis (.LNK) malveillants.
*   **Technique LOLBAS :** Détournement de l'utilitaire légitime `ftp.exe` pour exécuter des scripts de reconstruction de charge utile.
*   **Payload :** QUICAgent, un implant développé en Go utilisant le protocole QUIC (sur le port UDP 443) pour communiquer avec son serveur C2.
*   **Évasion :** Utilisation de délais aléatoires et d'opérations de hachage intensives (SHA-256) pour contourner les analyses en bac à sable (sandbox).
*   **Persistance :** Création d'un raccourci dans le dossier de démarrage (Startup) de l'utilisateur.

**Vulnérabilités :**
Aucune CVE spécifique n'est citée. L'attaque repose sur l'abus de fonctionnalités système légitimes (LOLBAS) et l'ingénierie sociale (fichiers LNK masqués en documents PDF).

**Recommandations :**
*   **Sensibilisation :** Former les utilisateurs à la méfiance envers les pièces jointes non sollicitées, en particulier les fichiers .LNK, .ISO ou .VHD reçus par e-mail.
*   **Filtrage réseau :** Surveiller les flux inhabituels utilisant le protocole QUIC (UDP 443) vers des destinations inconnues, et restreindre les communications sortantes.
*   **Politiques de sécurité :** Restreindre l'exécution de scripts et d'utilitaires système (`ftp.exe`) via des solutions de contrôle d'application (AppLocker ou EDR).
*   **Analyse comportementale :** Configurer les solutions de sécurité pour détecter les anomalies lors de l'exécution de processus, notamment lorsqu'un binaire signé tente de reconstruire des fichiers cachés dans des répertoires temporaires ou système.

---
[Source](https://thehackernews.com/2026/08/operation-quicsilver-targets-myanmar.html){:target="_blank"}
