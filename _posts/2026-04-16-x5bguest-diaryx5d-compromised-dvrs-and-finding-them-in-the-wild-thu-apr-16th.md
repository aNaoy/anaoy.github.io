---
title: '&#x5b;Guest Diary&#x5d; Compromised DVRs and Finding Them in the Wild, (Thu, Apr 16th)'
date: 2026-04-16
permalink: /posts/2026/04/16/x5bguest-diaryx5d-compromised-dvrs-and-finding-them-in-the-wild-thu-apr-16th/
tags:
- veille-cyber
- sans-isc
---
### Vulnérabilité et compromission massive des enregistreurs vidéo (DVR)

Les enregistreurs vidéo numériques (DVR) exposés sur Internet constituent des cibles privilégiées pour les attaquants, en raison de leur faible niveau de sécurisation et de l'usage persistant de mots de passe par défaut. Une analyse montre que des systèmes, tels que les modèles Airspace/Dahua, sont compromis par des scripts automatisés en moins de deux secondes via le port Telnet (23).

**Points clés :**
*   **Automatisation rapide :** Les attaques utilisent des scripts automatisés pour détecter la configuration du système, tester les droits d'écriture et vérifier les outils de téléchargement (TFTP, Wget) en un temps record.
*   **Persistance de l'infection :** L'analyse montre qu'environ 3,8 % des appareils identifiés via Shodan présentent des signes d'abus récents, suggérant des centaines de dispositifs déjà détournés pour servir de serveurs malveillants.
*   **Techniques d'évasion :** Les attaquants utilisent le répertoire `/dev/shm` (système de fichiers en mémoire vive) pour éviter les traces forensiques sur le disque et effacent les fichiers temporaires après leur exécution.
*   **Obsolescence :** Les appareils concernés utilisent souvent des firmwares très anciens (ex: 2014), rendant le correctif impossible ou négligé par les utilisateurs.

**Vulnérabilités exploitées :**
*   **Accès Telnet non sécurisé :** Utilisation du protocole Telnet (clair, non chiffré) exposé publiquement.
*   **Identifiants par défaut :** Usage de comptes "root/root" ou "admin/admin", largement documentés.
*   **Techniques MITRE ATT&CK identifiées :** T1110.001 (Password Guessing), T1078 (Valid Accounts), T1059.004 (Unix Shell), T1082 (System Information Discovery), T1564.001 (Hidden Files) et T1105 (Ingress Tool Transfer).

**Recommandations :**
*   **Restriction d'accès :** Désactiver l'accès Telnet sur Internet. Utiliser exclusivement un VPN ou un pare-feu local pour restreindre les connexions à des adresses IP de confiance.
*   **Durcissement des comptes :** Modifier systématiquement tous les mots de passe par défaut et désactiver les connexions root à distance.
*   **Gestion du cycle de vie :** Mettre à jour régulièrement le firmware des appareils de surveillance ou isoler ces équipements sur un réseau distinct sans accès direct à l'extérieur.

---
[Source](https://isc.sans.edu/diary/rss/32886){:target="_blank"}
