---
title: 'New GPUBreach attack enables system takeover via GPU rowhammer'
date: 2026-04-07
permalink: /posts/2026/04/07/new-gpubreach-attack-enables-system-takeover-via-gpu-rowhammer/
tags:
- veille-cyber
- bleepingcomp
---
### GPUBreach : Une nouvelle menace critique par Rowhammer sur GPU

**Points clés :**
*   **Vulnérabilité exploitée :** La technique Rowhammer est utilisée pour induire des basculements de bits (bit-flips) dans la mémoire GDDR6 des cartes graphiques.
*   **Mécanisme d'attaque :** En corrompant les tables de pages (PTE) du GPU, un noyau CUDA non privilégié obtient un accès arbitraire en lecture/écriture à la mémoire GPU.
*   **Escalade de privilèges :** L'attaque enchaîne cette corruption avec des failles de sécurité mémoire présentes dans les pilotes NVIDIA, permettant de compromettre l'intégralité du système (jusqu'à obtenir un accès root).
*   **Incontournable :** Contrairement aux attaques DMA classiques, GPUBreach réussit même lorsque la protection IOMMU (Input-Output Memory Management Unit) est active.

**Vulnérabilités :**
*   Aucun identifiant CVE spécifique n'est mentionné dans l'article, bien que l'attaque exploite des failles de sécurité mémoire découvertes au sein du pilote NVIDIA.

**Recommandations :**
*   **Activer l'ECC :** Activer les codes de correction d'erreurs (ECC) au niveau système, une mesure efficace pour bloquer les tentatives Rowhammer. Cette option est activée par défaut sur les gammes de GPU Data Center (Hopper et Blackwell).
*   **Limites de protection :** Ne pas se reposer exclusivement sur l'IOMMU, car cette protection matérielle est insuffisante face à cette attaque.
*   **Vigilance :** Les GPU grand public, qui ne bénéficient généralement pas de la mémoire ECC, restent particulièrement vulnérables et sans atténuation directe connue. Une mise à jour des avis de sécurité de NVIDIA est attendue pour fournir des directives complémentaires.

---
[Source](https://www.bleepingcomputer.com/news/security/new-gpubreach-attack-enables-system-takeover-via-gpu-rowhammer/){:target="_blank"}
