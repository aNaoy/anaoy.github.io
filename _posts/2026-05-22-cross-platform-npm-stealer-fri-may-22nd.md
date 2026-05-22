---
title: 'Cross-Platform NPM Stealer, (Fri, May 22nd)'
date: 2026-05-22
permalink: /posts/2026/05/22/cross-platform-npm-stealer-fri-may-22nd/
tags:
- veille-cyber
- sans-isc
---
### Analyse d'un Stealer NPM Multiplateforme

Un malware Node.js hautement obfusqué, ciblant Windows (via WSL), macOS et Linux, a été identifié. Bien que sa couche d'exécution utilise des techniques d'obfuscation classiques (type `obfuscator.io`), les charges utiles malveillantes restent lisibles. Le malware communique avec un serveur de commande et contrôle (C2) lié au groupe "OtterCookie" (DPRK) via l'adresse IP `216.126.225.243`.

#### Points clés
*   **Modules malveillants :**
    *   **Vol de credentials :** Cible les données de navigateurs populaires (Chrome, Edge, Brave, etc.) et une vaste liste d'extensions de portefeuilles de cryptomonnaies.
    *   **Exfiltration de fichiers :** Scan récursif du système de fichiers à la recherche de documents sensibles (clés privées, fichiers de configuration, seeds, documents personnels, bases de données, etc.).
    *   **C2 et Backdoor :** Établissement d'une connexion WebSocket pour offrir des capacités de "reverse-shell" à l'attaquant.
*   **Communication :** Utilisation de la bibliothèque `Axios` sur les ports 8085 (identifiants), 8086 (fichiers) et 8087 (C2).
*   **Faiblesse de chiffrement :** La clé utilisée pour le hachage HMAC (`SuperStr0ngSecret@)@^`) est codée en dur en clair dans le script.

#### Vulnérabilités et indicateurs
*   **CVE :** Aucune CVE spécifique n'est associée, le malware exploite le comportement légitime des applications pour accéder aux données locales.
*   **Indicateur réseau :** `216.126.225.243` (C2 associé à des menaces persistantes avancées).

#### Recommandations
*   **Filtrage réseau :** Bloquer les connexions sortantes vers l'adresse IP `216.126.225.243` et surveiller les flux sur les ports 8085, 8086 et 8087.
*   **Protection des endpoints :** Restreindre l'exécution de scripts Node.js non approuvés et surveiller l'accès aux dossiers de données des navigateurs (`User Data`).
*   **Gestion des secrets :** Ne jamais stocker de fichiers contenant des mots de passe, des clés privées ou des phrases de récupération (seed) en texte clair sur les machines de développement ou les postes de travail.
*   **Audit de dépendances :** Auditer les paquets NPM utilisés dans les projets pour détecter des injections malveillantes ou des dépendances suspectes.

---
[Source](https://isc.sans.edu/diary/rss/33006){:target="_blank"}
