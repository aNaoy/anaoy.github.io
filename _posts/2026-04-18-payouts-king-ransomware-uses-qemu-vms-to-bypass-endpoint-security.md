---
title: 'Payouts King ransomware uses QEMU VMs to bypass endpoint security'
date: 2026-04-18
permalink: /posts/2026/04/18/payouts-king-ransomware-uses-qemu-vms-to-bypass-endpoint-security/
tags:
- veille-cyber
- bleepingcomp
---
### L'utilisation détournée de QEMU par le ransomware Payouts King

Le ransomware Payouts King et le groupe affilié GOLD ENCOUNTER utilisent l'émulateur open-source QEMU pour déployer des machines virtuelles (VM) Alpine Linux dissimulées au sein des systèmes compromis. Cette technique permet aux attaquants de contourner les solutions de sécurité de l'hôte, d'exécuter des outils malveillants à l'abri des analyses et d'établir des tunnels SSH persistants pour un accès distant.

**Points clés :**
*   **Dissimulation :** Les attaquants créent des tâches planifiées (ex: "TPMProfiler") pour lancer des VM QEMU invisibles tournant avec des privilèges `SYSTEM`.
*   **Infrastructure malveillante :** Les VM hébergent des outils offensifs tels que Chisel, Rclone, AdaptixC2, ainsi que des frameworks complets (Metasploit, Impacket, BloodHound.py).
*   **Vecteurs d'accès :** Exploitation de vulnérabilités VPN (SonicWall, Cisco), phishing via Microsoft Teams (usurpation d'identité IT), abus de l'outil QuickAssist et exploitation de failles sur des équipements réseaux.
*   **Chiffrement :** Utilisation d'AES-256 (CTR) et RSA-4096, avec une stratégie de chiffrement intermittent pour accélérer la compromission des fichiers volumineux.

**Vulnérabilités exploitées :**
*   **CVE-2025-5777 :** Vulnérabilité critique dans Citrix NetScaler ADC et Gateway (CitrixBleed 2).
*   **CVE-2025-26399 :** Vulnérabilité dans SolarWinds Web Help Desk.

**Recommandations de sécurité :**
*   **Détection proactive :** Rechercher les installations non autorisées de QEMU, les fichiers de disques virtuels suspects (souvent déguisés en DLL ou bases de données) et les tâches planifiées s'exécutant avec des privilèges élevés.
*   **Surveillance réseau :** Identifier les transferts de données anormaux et les tunnels SSH sortants vers des ports non standards ou des adresses IP distantes.
*   **Durcissement :** Sécuriser les accès VPN par une authentification multi-facteurs (MFA) robuste et limiter l'exposition des outils d'administration à distance (comme QuickAssist ou ScreenConnect).

---
[Source](https://www.bleepingcomputer.com/news/security/payouts-king-ransomware-uses-qemu-vms-to-bypass-endpoint-security/){:target="_blank"}
