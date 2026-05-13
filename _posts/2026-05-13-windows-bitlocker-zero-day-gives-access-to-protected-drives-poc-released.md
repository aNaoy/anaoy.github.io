---
title: 'Windows BitLocker zero-day gives access to protected drives, PoC released'
date: 2026-05-13
permalink: /posts/2026/05/13/windows-bitlocker-zero-day-gives-access-to-protected-drives-poc-released/
tags:
- veille-cyber
- bleepingcomp
---
### Divulgation de failles Windows « YellowKey » et « GreenPlasma »

Un chercheur en sécurité, mécontent de la gestion des signalements de vulnérabilités par Microsoft, a publié des preuves de concept (PoC) pour deux failles non corrigées affectant Windows 11 et Windows Server 2022/2025.

**Points clés :**
*   **YellowKey :** Un contournement de BitLocker exploitant l'environnement de récupération Windows (WinRE). Il permet d'obtenir un accès illimité à un disque chiffré en manipulant des transactions NTFS via un support externe ou la partition EFI.
*   **GreenPlasma :** Une vulnérabilité d'élévation de privilèges (LPE) liée à la création arbitraire de sections mémoire via `ctfmon`, permettant théoriquement d'obtenir les privilèges `SYSTEM`.
*   **Contexte :** Ces fuites s'inscrivent dans une série de publications du chercheur « Chaotic Eclipse » (précédées par *BlueHammer* et *RedSun*), qui promet de nouvelles révélations pour le prochain *Patch Tuesday*.

**Vulnérabilités :**
*   **YellowKey :** Contournement de chiffrement BitLocker (pas de CVE attribué).
*   **GreenPlasma :** Élévation de privilèges (pas de CVE attribué).
*   **Note :** Les précédentes failles mentionnées incluent *BlueHammer* (CVE-2026-33825).

**Recommandations :**
*   **Pour YellowKey :** Bien que l'exploit actuel ne fonctionne qu'avec des configurations TPM-only, l'utilisation combinée d'un **code PIN BitLocker et d'un mot de passe BIOS** est fortement recommandée pour renforcer la sécurité.
*   **Veille :** Surveiller les mises à jour de sécurité de Microsoft, car des correctifs silencieux ou officiels pourraient être déployés prochainement pour ces composants.
*   **Limitation d'accès :** Restreindre physiquement l'accès aux ports USB et sécuriser le démarrage (Secure Boot) pour prévenir l'injection de fichiers malveillants sur les partitions EFI.

---
[Source](https://www.bleepingcomputer.com/news/security/windows-bitlocker-zero-day-gives-access-to-protected-drives-poc-released/){:target="_blank"}
