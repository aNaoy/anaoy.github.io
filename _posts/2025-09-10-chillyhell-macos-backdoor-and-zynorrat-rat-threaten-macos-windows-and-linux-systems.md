---
title: 'CHILLYHELL macOS Backdoor and ZynorRAT RAT Threaten macOS, Windows, and Linux Systems'
date: 2025-09-10
permalink: /posts/2025/09/10/chillyhell-macos-backdoor-and-zynorrat-rat-threaten-macos-windows-and-linux-systems/
tags:
- veille-cyber
- hackernews
---
**Nouvelles Menaces : CHILLYHELL et ZynorRAT Ciblent Multiples Systèmes d'Exploitation**

Deux nouvelles familles de malwares ont été identifiées, représentant des menaces significatives pour les systèmes d'exploitation macOS, Windows et Linux.

**CHILLYHELL : Une Porte Dérobée Sophistiquée pour macOS**

Ce malware, développé en C++ et attribué au groupe UNC4487 actif depuis au moins octobre 2022, cible spécifiquement les architectures Intel de macOS. UNC4487 est suspecté d'être un acteur d'espionnage compromettant des entités gouvernementales ukrainiennes pour distribuer CHILLYHELL via des techniques d'ingénierie sociale.

*   **Fonctionnalités Clés :**
    *   Collecte d'informations sur l'hôte compromis.
    *   Mise en place de trois mécanismes de persistance différents, incluant les LaunchAgents/LaunchDaemons et la modification des fichiers de profil shell (.zshrc, .bash_profile, .profile).
    *   Communication C2 via HTTP ou DNS avec des serveurs prédéfinis (93.88.75[.]252 ou 148.72.172[.]53).
    *   Utilisation du "timestomping" pour masquer la date de création des fichiers infectés, en utilisant des appels système directs ou des commandes `touch`.
    *   Exécution d'une large gamme de commandes : ouverture de reverse shell, téléchargement de nouvelles versions du malware ou de charges utiles supplémentaires, énumération des comptes utilisateurs et attaques par force brute de mots de passe.
    *   Structure modulaire offrant une grande flexibilité.
    *   Notarisation par Apple, démontrant que le code malveillant peut être signé.

*   **Recommandations :**
    *   Bien que non explicitement détaillées dans l'article, la mention de la notarisation par Apple souligne la nécessité d'une vigilance accrue quant aux certificats et au contenu des applications.

**ZynorRAT : Un Trojan d'Accès à Distance Basé sur Go**

Développé en langage Go, ZynorRAT est un RAT capable de cibler les systèmes Windows et Linux. Il utilise un bot Telegram (@lraterrorsbot) comme infrastructure principale de commande et contrôle (C2).

*   **Fonctionnalités Clés (Linux) :**
    *   Exfiltration de fichiers (`/fs_get`).
    *   Énumération de répertoires (`/fs_list`).
    *   Collecte d'informations système (`/metrics`).
    *   Lancement de commandes Linux (`ps`, `/proc_list`).
    *   Terminaison de processus (`/proc_kill` via PID).
    *   Capture d'écran (`/capture_display`).
    *   Mise en place de persistance via les services systemd (`/persist`).

*   **Fonctionnalités Clés (Windows) :**
    *   La version Windows est similaire à celle de Linux, mais semble encore en développement, utilisant des mécanismes de persistance inspirés de Linux.

*   **Distribution et Gestion :**
    *   Les charges utiles sont distribuées via le service de partage de fichiers Dosya.co.
    *   La gestion centrale s'effectue via le bot Telegram, qui transmet les commandes.
    *   L'auteur semble être un acteur isolé, potentiellement d'origine turque.

*   **Recommandations :**
    *   Surveillance des communications C2, notamment celles impliquant Telegram.
    *   Prudence lors du téléchargement de fichiers depuis des services de partage.
    *   Mise à jour régulière des systèmes d'exploitation et des logiciels de sécurité.

Aucune vulnérabilité spécifique avec des identifiants CVE n'est directement mentionnée pour ces deux malwares dans l'article.

---
[Source](https://thehackernews.com/2025/09/chillyhell-macos-backdoor-and-zynorrat.html){:target="_blank"}
