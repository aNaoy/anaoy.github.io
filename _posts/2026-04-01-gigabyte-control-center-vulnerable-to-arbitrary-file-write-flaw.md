---
title: 'GIGABYTE Control Center vulnerable to arbitrary file write flaw'
date: 2026-04-01
permalink: /posts/2026/04/01/gigabyte-control-center-vulnerable-to-arbitrary-file-write-flaw/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilité critique dans GIGABYTE Control Center

Le logiciel GIGABYTE Control Center (GCC), outil de gestion matérielle préinstallé sur les ordinateurs et cartes mères de la marque, présente une faille de sécurité majeure liée à sa fonctionnalité de « couplage » (pairing).

**Points clés :**
* **Nature du risque :** La vulnérabilité permet à un attaquant distant non authentifié d'écrire des fichiers arbitraires sur le système d'exploitation.
* **Conséquences :** Exécution de code à distance, élévation de privilèges et déni de service.
* **Systèmes affectés :** Versions du GCC 25.07.21.01 et antérieures lorsque l'option « pairing » est activée.

**Vulnérabilité identifiée :**
* **CVE-2026-4415 :** Score de sévérité critique de 9,2/10 (CVSS v4.0).

**Recommandations :**
* **Mise à jour immédiate :** Passer à la version **25.12.10.01** ou ultérieure, qui corrige la gestion des chemins de téléchargement, le traitement des messages et le chiffrement des commandes.
* **Sécurisation des sources :** Télécharger impérativement les mises à jour via le [portail officiel de GIGABYTE](https://www.gigabyte.com/consumer/software/gigabyte-control-center/global) pour éviter les installeurs malveillants.

---
[Source](https://www.bleepingcomputer.com/news/security/gigabyte-control-center-vulnerable-to-arbitrary-file-write-flaw/){:target="_blank"}
