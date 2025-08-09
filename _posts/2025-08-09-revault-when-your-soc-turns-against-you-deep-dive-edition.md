---
title: 'ReVault! When your SoC turns against you… deep dive edition'
date: 2025-08-09
permalink: /posts/2025/08/09/revault-when-your-soc-turns-against-you-deep-dive-edition/
tags:
- veille-cyber
- zerodaysfans
---
**Sécurité de Dell ControlVault : Une Analyse Approfondie**

Cette recherche explore en détail les vulnérabilités du Dell ControlVault, une solution de sécurité matérielle intégrée aux ordinateurs portables Dell. Le ControlVault, qui utilise le matériel Broadcom, gère les informations sensibles telles que les mots de passe et les données biométriques via une carte fille dédiée (Unified Security Hub - USH).

**Points Clés :**

*   **Cible Attrayante :** Le ControlVault est une cible intéressante en raison de son rôle dans la sécurité, de sa présence généralisée dans les ordinateurs portables professionnels et du fait que ses services Windows ne sont pas protégés par l'aléatoire de l'espace d'adressage (ASLR).
*   **Architecture Technique :** Le ControlVault repose sur la puce Broadcom 5820X et utilise un système d'exploitation temps réel (RTOS) appelé Citadel RTOS, potentiellement basé sur OpenRTOS. La communication avec le firmware se fait via USB et des commandes spécifiques (IOCTLs).
*   **Chiffrement du Firmware :** Le firmware applicatif du ControlVault est chiffré (AES-CBC) et son déchiffrement nécessite de retrouver les clés de chiffrement ou d'utiliser des valeurs par défaut codées en dur.
*   **Surface d'Attaque Étendue :** Le firmware expose plus de 150 commandes (CV Commands) pour interagir avec le système, créant une large surface d'attaque.
*   **Exécution de Code Arbitraire :** Des vulnérabilités ont été identifiées dans la gestion des sessions et le traitement des objets, permettant à un attaquant d'obtenir l'exécution de code arbitraire au niveau du firmware.
*   **Fuite de Clés et Modification du Firmware :** L'exécution de code dans le firmware permet de lire les clés OTP (One-Time Programmable) du dispositif, autorisant ainsi le déchiffrement du Secure Code Descriptor (SCD) et la création de firmwares personnalisés.
*   **Élévation de Privilèges :** Un firmware modifié peut être utilisé pour exploiter une vulnérabilité dans un service système Windows (BCMStorageAdapter.dll) via le framework Windows Biometric Framework (WBF), conduisant à une élévation de privilèges au niveau SYSTEM.
*   **Attaques Physiques :** Un accès physique à l'appareil permet de contourner certaines protections et de réaliser les attaques décrites, même sans être préalablement connecté au système d'exploitation.

**Vulnérabilités Identifiées :**

*   **CVE-2025-25215 :** Vulnérabilité de corruption de tas (heap corruption) dans les fonctions `cv_open` et `cv_close` due à une validation de session laxiste, permettant à un attaquant de déclencher une double libération de mémoire.
*   **CVE-2025-24922 :** Dépassement de tampon sur la pile (stack buffer overflow) dans la fonction `securebio_identify` lors de la copie de données d'un objet, pouvant mener à l'exécution de code arbitraire dans le firmware.
*   **CVE-2025-24311 :** Lecture hors limites dans la fonction `cv_send_blockdata`.
*   **CVE-2025-25050 :** Écriture hors limites dans la fonction `cv_upgrade_sensor_firmware`.
*   **CVE-2025-24919 :** Désérialisation non sécurisée lors de la communication host-firmware, en particulier dans la fonction `cv_get_object`, pouvant mener à un dépassement de tampon sur la pile sur le système hôte.

**Recommandations :**

*   **Surveillance des Services :** Surveiller les processus Windows qui chargent `bcmbipdll.dll` ou qui tentent d'ouvrir des handles vers le dispositif ControlVault.
*   **Vérification des Mises à Jour :** Vérifier l'intégrité des mises à jour du firmware ControlVault en s'assurant qu'elles s'installent correctement et que la version rapportée est attendue.
*   **Surveillance des Crashs :** Surveiller les crashs inattendus des services liés au ControlVault tels que `WinBioSvc`, `bcmHostStorageService`, `bcmHostControlService` ou `bcmUshUpgradeService`.
*   **Sécurisation Physique :** Appliquer des mesures de sécurité physique pour empêcher l'accès non autorisé aux composants internes de l'ordinateur portable.
*   **Mises à Jour du Firmware :** Maintenir le firmware du ControlVault à jour avec les derniers correctifs de sécurité fournis par Dell.

---
[Source](https://blog.talosintelligence.com/revault-when-your-soc-turns-against-you-2/){:target="_blank"}
