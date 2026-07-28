---
title: 'Tengu Botnet Reboots Compromised Linux Devices When Defenders Kill Its Process'
date: 2026-07-28
permalink: /posts/2026/07/28/tengu-botnet-reboots-compromised-linux-devices-when-defenders-kill-its-process/
tags:
- veille-cyber
- hackernews
---
### Tengu : Un botnet Linux sophistiqué doté de mécanismes d'auto-défense persistants

**Points clés :**
*   **Origine :** Tengu est un nouveau botnet dérivé de Mirai ciblant les systèmes Linux et potentiellement les appareils Android (via APK).
*   **Fonctionnalités :** Supporte 25 méthodes d'attaque DDoS, proxy SOCKS5, exécution de commandes shell, collecte de données et capacités d'auto-mise à jour.
*   **Vecteur d'infection :** Attaques par force brute sur le service Telnet.
*   **Ingénierie inverse :** Utilise un système de chiffrement ChaCha20/Poly1305 pour les commandes reçues du C2 et exploite une passerelle IPFS pour récupérer des charges utiles.
*   **Technique d'évasion :** Le malware corrompt les utilitaires système (reboot/shutdown) en modifiant leurs en-têtes ELF avec la chaîne « ELFOOD », empêchant ainsi les administrateurs de redémarrer correctement les appareils.

**Vulnérabilités :**
*   **Force brute Telnet :** Exploitation de services d'administration exposés sur internet avec des identifiants par défaut ou faibles.
*   **Aucune CVE spécifique identifiée :** L'infection repose sur la mauvaise configuration des périphériques IoT (ex: Android TV, routeurs) plutôt que sur une faille logicielle unique.

**Recommandations :**
*   **Réduction de la surface d'attaque :** Désactiver les services d'administration inutiles (Telnet) et remplacer systématiquement les identifiants par défaut par des mots de passe robustes.
*   **Mise à jour et segmentation :** Appliquer les correctifs de firmware et isoler les périphériques IoT sur des réseaux segmentés pour limiter la propagation latérale.
*   **Audit post-compromission :** Avant toute remise en service d'un appareil suspect, inspecter minutieusement les fichiers suivants :
    *   Services `systemd` et scripts `init`/`rc`.
    *   Fichiers de démarrage du shell.
    *   Tâches planifiées (cron).
    *   Vérifier l'intégrité des binaires système.
*   **Surveillance :** Surveiller les communications vers des ports non standards et les tentatives de connexion sortantes vers des serveurs C2 inconnus.

---
[Source](https://thehackernews.com/2026/07/tengu-botnet-reboots-compromised-linux.html){:target="_blank"}
