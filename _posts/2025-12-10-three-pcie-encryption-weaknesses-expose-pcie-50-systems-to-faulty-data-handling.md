---
title: 'Three PCIe Encryption Weaknesses Expose PCIe 5.0+ Systems to Faulty Data Handling'
date: 2025-12-10
permalink: /posts/2025/12/10/three-pcie-encryption-weaknesses-expose-pcie-50-systems-to-faulty-data-handling/
tags:
- veille-cyber
- hackernews
---
**Vulnérabilités dans le chiffrement PCIe : Risques pour les systèmes 5.0+**

Trois faiblesses ont été identifiées dans le protocole PCIe Integrity and Data Encryption (IDE), impactant la spécification PCIe Base 5.0 et suivantes. Ces vulnérabilités, découvertes par des employés d'Intel, peuvent permettre à un attaquant local d'obtenir des informations, d'escalader ses privilèges ou de provoquer un déni de service en manipulant des données transmises via l'interface PCIe.

**Points clés :**

*   Le protocole IDE a été introduit pour sécuriser les transferts de données sur les interfaces PCIe.
*   Ces faiblesses concernent spécifiquement les systèmes implémentant l'IDE et le Trusted Domain Interface Security Protocol (TDISP).
*   L'exploitation nécessite un accès physique ou de bas niveau à l'interface PCIe IDE de la cible.

**Vulnérabilités identifiées :**

*   **CVE-2025-9612 (Forbidden IDE Reordering)** : Une vérification d'intégrité manquante sur un port récepteur peut permettre le réordonnancement du trafic PCIe, amenant le récepteur à traiter des données obsolètes.
*   **CVE-2025-9613 (Completion Timeout Redirection)** : Une opération de vidage incomplète d'un délai d'attente de complétion peut permettre à un récepteur d'accepter des données incorrectes lorsqu'un attaquant injecte un paquet avec une étiquette correspondante.
*   **CVE-2025-9614 (Delayed Posted Redirection)** : Un vidage ou un renouvellement incomplet de clé d'un flux IDE peut entraîner la consommation par le récepteur de paquets de données obsolètes ou incorrects.

Ces vulnérabilités sont considérées comme de faible sévérité en raison des prérequis d'accès.

**Recommandations :**

*   Les fabricants doivent suivre la norme PCIe 6.0 mise à jour et appliquer les directives de l'Erratum #1 à leurs implémentations IDE.
*   Les utilisateurs finaux doivent installer les mises à jour de firmware fournies par leurs fournisseurs de systèmes ou de composants, particulièrement dans les environnements où l'IDE est utilisé pour protéger des données sensibles.

Les processeurs Intel Xeon 6 (avec P-cores) et les processeurs AMD EPYC 9005 Series sont notamment concernés.

---
[Source](https://thehackernews.com/2025/12/three-pcie-encryption-weaknesses-expose.html){:target="_blank"}
