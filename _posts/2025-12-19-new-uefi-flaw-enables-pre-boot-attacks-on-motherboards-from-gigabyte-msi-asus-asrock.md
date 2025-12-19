---
title: 'New UEFI flaw enables pre-boot attacks on motherboards from Gigabyte, MSI, ASUS, ASRock'
date: 2025-12-19
permalink: /posts/2025/12/19/new-uefi-flaw-enables-pre-boot-attacks-on-motherboards-from-gigabyte-msi-asus-asrock/
tags:
- veille-cyber
- bleepingcomp
---
### Failles UEFI : Accès non autorisé à la mémoire avant le démarrage

Des vulnérabilités dans le micrologiciel UEFI de cartes mères ASUS, Gigabyte, MSI et ASRock permettent des attaques par accès direct à la mémoire (DMA) avant le chargement du système d'exploitation. Ces failles peuvent contourner les protections mémoire initiales, laissant le système exposé.

**Points Clés :**

*   L'unité de gestion mémoire d'entrée/sortie (IOMMU), censée protéger la RAM, n'est pas correctement initialisée lors des premières étapes du démarrage sur les systèmes affectés.
*   Cela crée une fenêtre où des appareils PCIe malveillants, connectés physiquement, peuvent lire ou modifier la mémoire système sans être détectés par les outils de sécurité.
*   Certains jeux, comme Valorant, refusent de se lancer sur ces systèmes vulnérables en raison de la protection de leur système anti-triche Vanguard.

**Vulnérabilités :**

*   CVE-2025-11901
*   CVE-2025-14302
*   CVE-2025-14303
*   CVE-2025-14304

**Recommandations :**

*   Vérifier et installer les mises à jour du micrologiciel (UEFI) fournies par les fabricants (ASUS, Gigabyte, MSI, ASRock) pour les modèles concernés.
*   Il est conseillé de sauvegarder les données importantes avant d'appliquer les mises à jour du micrologiciel.

---
[Source](https://www.bleepingcomputer.com/news/security/new-uefi-flaw-enables-pre-boot-attacks-on-motherboards-from-gigabyte-msi-asus-asrock/){:target="_blank"}
