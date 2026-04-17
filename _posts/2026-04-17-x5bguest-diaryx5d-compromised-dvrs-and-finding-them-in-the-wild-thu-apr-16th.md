---
title: '&#x5b;Guest Diary&#x5d; Compromised DVRs and Finding Them in the Wild, (Thu, Apr 16th)'
date: 2026-04-17
permalink: /posts/2026/04/17/x5bguest-diaryx5d-compromised-dvrs-and-finding-them-in-the-wild-thu-apr-16th/
tags:
- veille-cyber
- sans-isc
---
### Vulnérabilité et compromission des enregistreurs vidéo (DVR) exposés

Les enregistreurs vidéo numériques (DVR), particulièrement les anciens modèles (ex: Airspace/Dahua), constituent une cible privilégiée pour les attaquants en raison de leur exposition sur Internet et de leur maintenance quasi inexistante. Cette analyse met en lumière la rapidité avec laquelle des systèmes mal protégés sont infiltrés via des attaques automatisées.

**Points clés :**
* **Automatisation des attaques :** Les compromissions se produisent en quelques secondes (environ 2 secondes pour une session complète). L'attaquant utilise des scripts pour identifier les vulnérabilités du système et préparer l'environnement avant le déploiement d'une charge utile malveillante.
* **Vecteur d'accès :** L'utilisation massive du protocole Telnet (port 23) avec des identifiants par défaut (ex: `root/root`, `admin/admin`).
* **Permanence des menaces :** Une fois le système compromis, il sert de serveur pour les activités illicites des attaquants. Une étude extrapolée suggère que plusieurs centaines de ces appareils sont déjà compromis à l'échelle mondiale.
* **Techniques observées (MITRE ATT&CK) :**
    * **T1110.001 / T1078 :** Force brute et utilisation de comptes valides par défaut.
    * **T1059.004 :** Accès à un shell Unix.
    * **T1082 / T1564.001 :** Découverte du système, vérification des capacités d'exécution et utilisation de fichiers cachés (`/dev/shm`) pour échapper à la détection médico-légale.
    * **T1105 :** Préparation au transfert d'outils (recherche de `wget` ou `tftp`).

**Vulnérabilités :**
* Aucune CVE spécifique n'est mentionnée, mais le risque repose sur des **vulnérabilités de configuration critique** :
    * Utilisation de mots de passe par défaut documentés.
    * Absence de mises à jour de firmware depuis plusieurs années (ex: obsolescence depuis 2014).
    * Exposition de services d'administration (Telnet, interfaces web) sur le réseau public.

**Recommandations :**
* **Isolation réseau :** Restreindre strictement l'accès Telnet via un pare-feu ou un VPN pour limiter l'exposition à Internet.
* **Gestion des accès :** Modifier immédiatement tous les mots de passe par défaut par des identifiants robustes et désactiver la connexion `root` à distance via Telnet.
* **Maintien en condition opérationnelle :** Appliquer régulièrement les correctifs de sécurité fournis par le constructeur et remplacer les équipements dont le firmware n'est plus supporté.

---
[Source](https://isc.sans.edu/diary/rss/32886){:target="_blank"}
