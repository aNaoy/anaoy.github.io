---
title: 'Disabling Security Features in a Locked BIOS'
date: 2026-03-26
permalink: /posts/2026/03/26/disabling-security-features-in-a-locked-bios/
tags:
- veille-cyber
- zerodaysfans
---
### Contournement de la sécurité UEFI par injection DMA

Cette recherche démontre une méthode pour désactiver les protections DMA (Direct Memory Access) au niveau du firmware sur des appareils Dell, même lorsque le BIOS est protégé par un mot de passe. En modifiant directement l'image UEFI (patch de la NVRAM), un attaquant peut contourner le chiffrement BitLocker (TPM-only) et obtenir un accès système complet (NT AUTHORITY\SYSTEM) sans authentification.

**Points clés**
*   **Dissimulation :** La modification du firmware ne change pas l'interface graphique du BIOS ; le réglage apparaît comme « activé » alors qu'il est fonctionnellement désactivé.
*   **Persistance :** La modification peut survivre aux mises à jour officielles du firmware.
*   **Méthodologie :** Extraction du dump SPI via programmeur externe/interne, identification du module de configuration via `UEFITool` et `IFRExtractor`, puis modification hexadécimale de l'offset NVRAM correspondant au paramètre IOMMU.
*   **Exploitation :** Une fois le DMA activé, l'utilisation d'outils comme *DMAReaper* et *PCILeech* permet d'injecter du code dans la mémoire et de prendre le contrôle de la machine.

**Vulnérabilités**
*   **Absence de protection en écriture robuste :** La possibilité d'écrire sur la puce SPI permet d'altérer les paramètres de sécurité fondamentaux.
*   **Contournement des mesures de sécurité :** Modification offline de la configuration sans déclencher les mesures de démarrage sécurisé (Measured Boot) qui nécessiteraient normalement une clé de récupération BitLocker.
*   *Note : Aucune CVE spécifique n'est mentionnée, car il s'agit d'une faiblesse liée à la conception matérielle et au stockage des variables de configuration NVRAM.*

**Recommandations**
*   **Sécurisation physique :** Restreindre l'accès physique aux appareils pour éviter l'usage de programmeurs SPI sur la carte mère.
*   **Intégrité du matériel :** Utiliser des fonctionnalités de verrouillage de châssis ou des vis inviolables pour détecter toute ouverture physique.
*   **Chiffrement renforcé :** Privilégier la configuration TPM+PIN pour BitLocker afin d'ajouter un facteur d'authentification supplémentaire, limitant ainsi l'efficacité d'une attaque basée uniquement sur le DMA au démarrage.
*   **Surveillance :** Être conscient que les interfaces de configuration BIOS ne sont pas infaillibles face à une altération directe de la mémoire flash.

---
[Source](https://www.mdsec.co.uk/2026/03/disabling-security-features-in-a-locked-bios/){:target="_blank"}
