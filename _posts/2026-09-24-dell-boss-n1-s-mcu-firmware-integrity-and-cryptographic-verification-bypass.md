---
title: 'Dell BOSS-N1 S-MCU Firmware Integrity and Cryptographic Verification Bypass'
date: 2026-09-24
permalink: /posts/2026/09/24/dell-boss-n1-s-mcu-firmware-integrity-and-cryptographic-verification-bypass/
tags:
- veille-cyber
- zerodaysfans
---
### Vulnérabilités de l'intégrité du firmware du Dell BOSS-N1 S-MCU

Les recherches menées sur le contrôleur de stockage Dell BOSS-N1 S-MCU ont révélé des failles critiques permettant de contourner les mécanismes de sécurité et d'exécuter un firmware malveillant persistant.

#### Points clés
*   **Contournement de la Root-of-Trust :** Un attaquant peut manipuler le processus de mise à jour du firmware via l'interface I2C/SMBus. En modifiant les instructions ARM, il redirige les requêtes de lecture de l'iDRAC vers un emplacement mémoire inactif contenant un firmware sain. L'iDRAC valide alors ce code propre tandis que le processeur exécute le code malveillant modifié.
*   **Absence de signature cryptographique :** Le système repose uniquement sur des sommes de contrôle (checksums) facilement recalculables, et non sur une authentification cryptographique robuste.
*   **Interface de débogage exposée :** Le port SWD (Serial Wire Debug) est non protégé et sans restriction d'accès, facilitant le vidage mémoire et l'injection de code.

#### Vulnérabilités identifiées
*   **Bypass de la vérification cryptographique (iDRAC) :** Exploitation via l'interface I2C pour rediriger les vérifications d'intégrité (Sévérité élevée : 7.3 CVSS).
*   **Interface de débogage non protégée :** Accès physique ou via iDRAC compromis au port SWD sans authentification (Sévérité moyenne : 5.9 CVSS).
*   **Absence de vérification d'intégrité sur le SoC :** Le stockage du firmware ne vérifie pas l'authenticité du code exécuté (Sévérité élevée : 7.3 CVSS).

#### Recommandations
*   **Renforcement du firmware :** Mettre en œuvre une vérification par signature cryptographique pour toutes les mises à jour et les images stockées (R01, R06).
*   **Sécurisation des accès :** Restreindre strictement l'accès aux interfaces de mise à jour (I2C/SMBus) et désactiver ou protéger par mot de passe les interfaces de débogage (SWD/JTAG) en production (R02, R04).
*   **Surveillance :** Implémenter des contrôles d'intégrité plus stricts au niveau de l'iDRAC et monitorer toute utilisation anormale des interfaces de débogage (R03, R05).

---
[Source](https://github.com/google/security-research/security/advisories/GHSA-wcfm-jp7m-rffh){:target="_blank"}
