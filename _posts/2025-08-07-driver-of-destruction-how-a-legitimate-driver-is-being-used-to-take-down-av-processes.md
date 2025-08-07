---
title: 'Driver of destruction: How a legitimate driver is being used to take down AV processes'
date: 2025-08-07
permalink: /posts/2025/08/07/driver-of-destruction-how-a-legitimate-driver-is-being-used-to-take-down-av-processes/
tags:
- veille-cyber
- securelist
---
## Driverjacking : Le démantèlement des protections antivirus

Une nouvelle menace, active depuis octobre 2024, utilise le pilote système légitime `ThrottleStop.sys` pour désactiver les processus antivirus. Cette technique, connue sous le nom de BYOVD (Bring Your Own Vulnerable Driver), permet aux attaquants de contourner les défenses avant de déployer des malwares, comme une variante de MedusaLocker observée dans une attaque récente au Brésil. L'attaquant a initialement accédé au réseau via des identifiants RDP valides, puis a utilisé des outils comme Mimikatz et Invoke-WMIExec/Invoke-SMBExec pour se déplacer latéralement et désactiver les solutions de sécurité avant de chiffrer les données.

### Points Clés :

*   **Méthode d'attaque :** Utilisation d'un pilote signé légitimement mais vulnérable pour la désactivation des antivirus.
*   **Vecteur d'infection initial :** Accès via des identifiants RDP compromis.
*   **Mouvement latéral :** Technique de "pass-the-hash" avec Mimikatz et scripts PowerShell.
*   **Malware final :** Variantes de ransomware MedusaLocker et un utilitaire de mise à mort d'antivirus.
*   **Ciblage :** L'outil désactive une large gamme de produits antivirus.

### Vulnérabilités :

*   **CVE-2025-7771 :** Une vulnérabilité dans le pilote `ThrottleStop.sys` permettait des opérations de lecture/écriture en mémoire physique via des appels IOCTL à partir du mode utilisateur. Cela était rendu possible par la fonction `MmMapIoSpace`, exposant des primitives de lecture/écriture sur des adresses physiques.

### Recommandations :

*   **Renforcer la sécurité des accès distants :** Limiter l'accès RDP aux adresses IP publiques et imposer des politiques de mots de passe robustes.
*   **Mettre en œuvre la défense en profondeur :** Utiliser plusieurs couches de sécurité, y compris l'autorisation d'applications (whitelisting), des privilèges minimum, la segmentation réseau.
*   **Authentification multifacteur (MFA) :** Activer la MFA pour tous les canaux d'accès à distance.
*   **Gestion des correctifs :** Assurer une gestion régulière des correctifs et des analyses de vulnérabilités automatisées.
*   **Détection et réponse :** Déployer des systèmes de détection et de prévention d'intrusion (IDS/IPS) et des solutions de détection et de réponse sur les points de terminaison (EDR).
*   **Surveillance :** Mettre en place une journalisation complète, une surveillance et des alertes pour une détection rapide des incidents.
*   **Tests de sécurité :** Effectuer des évaluations de sécurité et des tests d'intrusion périodiques.
*   **Auto-défense des solutions de sécurité :** Les produits de protection doivent intégrer des mécanismes d'auto-défense pour empêcher la modification ou la terminaison de leurs processus.

Les indicateurs de compromission incluent le hachage du pilote vulnérable (`82ed942a52cdcf120a8919730e00ba37619661a3`) et les hachages des malwares observés. Les victimes principales ont été identifiées en Russie, Biélorussie, Kazakhstan, Ukraine et Brésil.

---
[Source](https://securelist.com/av-killer-exploiting-throttlestop-sys/117026/){:target="_blank"}
