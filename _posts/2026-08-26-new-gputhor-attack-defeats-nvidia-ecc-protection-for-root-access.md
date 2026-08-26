---
title: 'New GPUThor attack defeats NVIDIA ECC protection for root access'
date: 2026-08-26
permalink: /posts/2026/08/26/new-gputhor-attack-defeats-nvidia-ecc-protection-for-root-access/
tags:
- veille-cyber
- bleepingcomp
---
### GPUThor : Une nouvelle menace Rowhammer contre les GPU NVIDIA

Des chercheurs de l'Université de Toronto ont dévoilé **GPUThor**, une technique d'attaque de type *Rowhammer* capable de contourner les protections ECC (Error Correction Code) des GPU NVIDIA. En exploitant des comportements non documentés de la mémoire GDDR6, cette attaque permet de provoquer des inversions de bits massives, menant à des dénis de service (DoS) ou à une élévation de privilèges vers le niveau "root".

**Points clés :**
*   **Efficacité accrue :** GPUThor génère jusqu'à 23 000 fois plus d'erreurs que les méthodes précédentes (GPUHammer), réduisant le temps nécessaire à une exploitation fructueuse de plusieurs heures à environ 1,1 minute.
*   **Contournement ECC :** L'attaque utilise un schéma de martelage (*hammering*) non uniforme qui évite les mécanismes de rafraîchissement des lignes cibles (TRR). Elle peut induire des erreurs multi-bits que l'ECC actuel ne parvient pas à corriger correctement, entraînant une corruption des données.
*   **Impact critique :** En corrompant les tables de pages du GPU, un attaquant peut obtenir un accès arbitraire à la mémoire et ouvrir un shell root sur le système hôte.

**Vulnérabilités :**
*   **Cibles confirmées :** GPU NVIDIA de classe Ampere avec mémoire GDDR6 (RTX A4000, A4500, A5000, A6000).
*   **Vulnérabilité potentielle :** La menace plane également sur les GPU serveurs (A100) et potentiellement sur des architectures plus récentes (HBM3/e, GDDR7) si des basculements multi-bits sont déclenchés.
*   **Note :** Aucune CVE spécifique n'a été attribuée à ce stade dans l'article.

**Recommandations de sécurité :**
*   **Configuration système :** Activer systématiquement le mode SYS-ECC et l'isolation IOMMU/DMA.
*   **Gestion des workloads :** Éviter le partage de GPU entre plusieurs locataires (*cross-tenant*) et restreindre strictement l'exécution de programmes CUDA non fiables.
*   **Surveillance :** Surveiller activement les compteurs d'erreurs ECC pour détecter des tentatives d'attaque en temps réel.
*   **Conseil constructeur :** NVIDIA recommande de consulter son avis officiel pour des conseils d'atténuation spécifiques selon l'architecture matérielle utilisée.

---
[Source](https://www.bleepingcomputer.com/news/security/new-gputhor-attack-defeats-nvidia-ecc-protection-for-root-access/){:target="_blank"}
