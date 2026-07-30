---
title: 'Reconnaissance First: An SSH Bot That Sizes Up Your Hardware Before Deploying a Miner &#x5b;Guest Diary&#x5d;, (Thu, Jul 30th)'
date: 2026-07-30
permalink: /posts/2026/07/30/reconnaissance-first-an-ssh-bot-that-sizes-up-your-hardware-before-deploying-a-miner-x5bguest-diaryx5d-thu-jul-30th/
tags:
- veille-cyber
- sans-isc
---
### Analyse d'une reconnaissance ciblée avant déploiement de cryptomineur

Des attaques récentes observées sur des serveurs SSH démontrent une stratégie de « reconnaissance d'abord » : au lieu de déployer immédiatement un logiciel malveillant, les attaquants effectuent un audit matériel précis de la machine cible pour déterminer si elle est rentable pour le minage de cryptomonnaies.

**Points clés :**
*   **Stratégie de filtrage :** L'attaquant évalue la viabilité de la cible en mesurant les ressources (cœurs CPU, modèle de processeur, présence d'un GPU NVIDIA, mémoire vive supérieure à 1 Go).
*   **Vérification de privilèges :** Le bot utilise `sudo -S` pour confirmer qu'il peut obtenir des privilèges root sans interaction manuelle.
*   **Absence de charge utile immédiate :** La session se termine après quelques secondes sans téléchargement de fichier, ce qui permet à l'attaquant d'éviter la détection par les outils de sécurité classiques basés sur les signatures de fichiers.
*   **Utilisation de fingerprints :** L'usage d'identifiants SSH spécifiques (HASSH) permet de corréler ces sessions de reconnaissance discrètes avec des campagnes d'infection ultérieures.

**Vulnérabilités exploitées :**
*   **Identifiants faibles :** Utilisation de mots de passe triviaux (ex: `123123`) pour le compte `root`.
*   **Configuration SSH permissive :** Autorisation de connexion directe pour l'utilisateur `root`.

**Recommandations de sécurité :**
*   **Durcissement des accès :** Désactiver la connexion SSH pour l'utilisateur `root` (`PermitRootLogin no`) et privilégier l'authentification par clés cryptographiques.
*   **Politique de mots de passe :** Imposer des mots de passe robustes et uniques.
*   **Réduction de la surface d'attaque :** Limiter l'exposition du service SSH à Internet (utilisation de VPN ou filtrage par IP source).
*   **Surveillance comportementale :** 
    *   Mettre en place des alertes sur des séquences de commandes suspectes (lecture de `/proc/meminfo`, inventaire matériel via `lspci`).
    *   Utiliser `fail2ban` ou des solutions similaires pour limiter le taux de tentatives de connexion.
    *   Surveiller les pics de consommation CPU/GPU inattendus qui pourraient indiquer le déploiement tardif d'un mineur.

---
[Source](https://isc.sans.edu/diary/rss/33198){:target="_blank"}
