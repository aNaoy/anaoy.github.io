---
title: 'New Spirals ransomware encrypts victim network in under 24 hours'
date: 2026-07-16
permalink: /posts/2026/07/16/new-spirals-ransomware-encrypts-victim-network-in-under-24-hours/
tags:
- veille-cyber
- bleepingcomp
---
### Spirals : Une menace ransomware ultra-rapide

Le groupe cybercriminel « Spirals » a démontré une capacité d'exécution redoutable en compromettant une entreprise de services informatiques en moins de 24 heures, de l'intrusion initiale jusqu'au chiffrement des données.

**Points clés :**
* **Vitesse d'exécution :** Le cycle complet (accès, vol de données, chiffrement) est réalisé en moins d'une journée.
* **Technique de chiffrement :** Utilisation du langage Rust avec un chiffrement intermittent pour les fichiers de plus de 5 Mo afin d'accélérer le processus. Les clés AES-128 sont protégées par une clé publique ECDH P-256.
* **Persistance et mouvement latéral :** Utilisation de tunnels (Cloudflare, Chisel, revsocks) et de PowerShell pour désactiver les solutions de sécurité (Microsoft Defender) et arrêter les services critiques (Veeam, VMware, bases de données).
* **Masquage :** Le ransomware se déploie sous le nom de `bitsadmin.exe` pour imiter un utilitaire système légitime.

**Vulnérabilités exploitées :**
* **Accès initial :** Serveur IIS (Internet Information Services) exposé publiquement. Bien que non spécifiée par une CVE dans l'article, l'exploitation d'un serveur IIS public souligne une vulnérabilité classique de surface d'exposition non sécurisée ou mal patchée.
* **Élévation de privilèges :** Contournement de l'UAC (User Account Control) et extraction de secrets via le vidage de la mémoire LSASS et de la ruche SAM.

**Recommandations :**
* **Sécurisation de la surface d'exposition :** Restreindre strictement l'accès aux serveurs web publics et appliquer les correctifs de sécurité immédiatement.
* **Durcissement des systèmes :** Désactiver les services inutilisés, surveiller l'exécution de processus suspects et limiter les privilèges d'administration.
* **Protection des identifiants :** Mettre en œuvre des mesures pour empêcher l'extraction de mots de passe de la mémoire (Credential Guard) et surveiller les comportements anormaux liés aux services LSASS et SAM.
* **Sauvegardes :** Maintenir des sauvegardes isolées (hors ligne ou immuables) puisque les attaquants ciblent spécifiquement les logiciels de sauvegarde pour neutraliser les capacités de récupération.
* **Détection :** Utiliser des solutions de type EDR/XDR pour détecter les activités suspectes (tunnels de communication, désactivation de l'antivirus, exécution de PsExec).

---
[Source](https://www.bleepingcomputer.com/news/security/new-spirals-ransomware-encrypts-victim-network-in-under-24-hours/){:target="_blank"}
