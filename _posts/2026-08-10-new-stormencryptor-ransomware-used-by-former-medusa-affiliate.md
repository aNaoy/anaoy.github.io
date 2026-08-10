---
title: 'New StormEncryptor ransomware used by former Medusa affiliate'
date: 2026-08-10
permalink: /posts/2026/08/10/new-stormencryptor-ransomware-used-by-former-medusa-affiliate/
tags:
- veille-cyber
- bleepingcomp
---
### Émergence du ransomware StormEncryptor par le groupe Storm-1175

Le groupe cybercriminel Storm-1175, précédemment affilié au ransomware Medusa, a lancé une nouvelle souche de ransomware appelée **StormEncryptor**. Ce groupe, vraisemblablement basé en Chine, se distingue par sa capacité à exploiter rapidement des vulnérabilités critiques pour infiltrer, exfiltrer des données et déployer son logiciel malveillant en quelques jours seulement.

**Points clés :**
* **Mode opératoire :** Après l'accès initial, l'attaquant utilise des outils légitimes (AnyDesk, SimpleHelp, Advanced IP Scanner) pour la gestion à distance et la découverte réseau, ainsi que Mimikatz pour le vol d'identifiants (LSASS).
* **Impact :** Les fichiers sont chiffrés avec l'extension `.encrypted` et une demande de rançon (`!!!README_FIRST!!!.txt`) exige un paiement sous trois jours, sous peine de fuite des données volées.
* **Vecteur d'attaque :** L'intrusion récente repose sur l'exploitation d'une vulnérabilité de contournement d'authentification dans l'outil RMM N-central de N-able.

**Vulnérabilité exploitée :**
* **CVE-2026-18577 :** Vulnérabilité de contournement d'authentification dans N-able N-central.

**Recommandations :**
* **Mise à jour immédiate :** Appliquer le correctif (hotfix 2026.3 HF1 / build 2026.3.1.7) fourni par N-able.
* **Surveillance proactive :** Rechercher des signes de compromission, notamment la présence du fichier `svchost.exe` dans les dossiers "Documents", un service enregistré sous le nom `Cloudflared` et des connexions entrantes suspectes provenant d'adresses IP non autorisées.
* **Sécurisation :** Maintenir une veille constante sur les vulnérabilités de type *zero-day* et *n-day*, le groupe Storm-1175 étant historiquement habitué à cibler des failles dans des logiciels critiques (GoAnywhere MFT, Microsoft Exchange, etc.).

---
[Source](https://www.bleepingcomputer.com/news/security/new-stormencryptor-ransomware-used-by-former-medusa-affiliate/){:target="_blank"}
