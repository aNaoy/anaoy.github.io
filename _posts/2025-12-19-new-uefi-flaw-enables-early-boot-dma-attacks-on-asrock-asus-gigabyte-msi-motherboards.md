---
title: 'New UEFI Flaw Enables Early-Boot DMA Attacks on ASRock, ASUS, GIGABYTE, MSI Motherboards'
date: 2025-12-19
permalink: /posts/2025/12/19/new-uefi-flaw-enables-early-boot-dma-attacks-on-asrock-asus-gigabyte-msi-motherboards/
tags:
- veille-cyber
- hackernews
---
## Attaques DMA précoces sur cartes mères

Une faille dans certaines implémentations du firmware UEFI sur des cartes mères ASRock, ASUS, GIGABYTE et MSI permet des attaques par accès direct à la mémoire (DMA) en début de démarrage. Bien que la protection DMA soit indiquée comme active, l'unité de gestion de mémoire d'entrée/sortie (IOMMU) n'est pas correctement configurée et activée durant cette phase critique. Cela ouvre la porte à des périphériques malveillants, ayant un accès physique, pour lire ou modifier la mémoire système avant même que le système d'exploitation et ses protections ne soient chargés.

**Points Clés :**

*   La vulnérabilité exploite une défaillance de configuration de l'IOMMU pendant le démarrage.
*   Elle permet des modifications de la mémoire système avant le chargement du système d'exploitation.
*   Les attaquants avec un accès physique peuvent potentiellement injecter du code malveillant ou voler des données sensibles.

**Vulnérabilités :**

*   **CVE-2025-14304** (CVSS 7.0) : Affecte les cartes mères ASRock (Intel 500, 600, 700, 800 series chipsets).
*   **CVE-2025-11901** (CVSS 7.0) : Affecte les cartes mères ASUS (Intel Z490, W480, B460, H410, Z590, B560, H510, Z690, B660, W680, Z790, B760, W790 series chipsets).
*   **CVE-2025-14302** (CVSS 7.0) : Affecte les cartes mères GIGABYTE (Intel Z890, W880, Q870, B860, H810, Z790, B760, Z690, Q670, B660, H610, W790 series chipsets; AMD X870E, X870, B850, B840, X670, B650, A620, A620A, TRX50 series chipsets).
*   **CVE-2025-14303** (CVSS 7.0) : Affecte les cartes mères MSI (Intel 600 et 700 series chipsets).

**Recommandations :**

*   Les fabricants concernés publient des mises à jour de firmware pour corriger l'initialisation de l'IOMMU.
*   Il est essentiel que les utilisateurs et administrateurs appliquent ces mises à jour dès leur disponibilité pour se protéger contre cette menace.
*   Dans les environnements où l'accès physique ne peut être totalement contrôlé, une application rapide des correctifs et le respect des bonnes pratiques de sécurité matérielle sont cruciaux.

---
[Source](https://thehackernews.com/2025/12/new-uefi-flaw-enables-early-boot-dma.html){:target="_blank"}
