---
title: 'ReVault flaws let hackers bypass Windows login on Dell laptops'
date: 2025-08-06
permalink: /posts/2025/08/06/revault-flaws-let-hackers-bypass-windows-login-on-dell-laptops/
tags:
- veille-cyber
- bleepingcomp
---
**Sécurité des ordinateurs portables Dell : le firmware ReVault compromis**

Des failles de sécurité dans le firmware ControlVault3 de Dell, regroupées sous le nom de "ReVault", affectent plus de 100 modèles d'ordinateurs portables, permettant aux attaquants de contourner l'authentification Windows et d'installer des logiciels malveillants persistants, même après une réinstallation du système. Ces vulnérabilités touchent les séries Latitude et Precision, utilisées dans des environnements critiques tels que la cybersécurité et le gouvernement.

**Points clés :**

*   Les failles exploitent la solution de sécurité matérielle ControlVault3, qui gère les données d'authentification sensibles.
*   L'accès physique à l'appareil permet à un attaquant de cibler directement la carte Unified Security Hub (USH).
*   Les vulnérabilités permettent l'exécution de code arbitraire sur le firmware, la création d'implants persistants, le contournement de la connexion Windows et l'escalade de privilèges.
*   L'exploitation peut également manipuler l'authentification par empreinte digitale pour accepter toute empreinte.

**Vulnérabilités identifiées (ReVault) :**

*   Dépassements de tampon (CVE-2025-24311, CVE-2025-25050)
*   Vulnérabilité d'allocation mémoire arbitraire (CVE-2025-25215)
*   Dépassement de pile (CVE-2025-24922)
*   Désérialisation non sécurisée (CVE-2025-24919)

**Recommandations :**

*   Installer les mises à jour de sécurité fournies par Dell pour le firmware et les pilotes ControlVault3.
*   Désactiver les périphériques de sécurité inutilisés tels que les lecteurs d'empreintes digitales, de cartes à puce et NFC.
*   Désactiver la connexion par empreinte digitale dans les situations à haut risque.
*   Activer la détection d'intrusion du châssis dans les paramètres du BIOS pour signaler les tentatives de manipulation physique.
*   Activer la "Enhanced Sign-in Security" (ESS) dans Windows pour détecter les firmwares CV inappropriés.

---
[Source](https://www.bleepingcomputer.com/news/security/revault-flaws-let-hackers-bypass-windows-login-on-dell-laptops/){:target="_blank"}
