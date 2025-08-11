---
title: 'New TETRA Radio Encryption Flaws Expose Law Enforcement Communications'
date: 2025-08-11
permalink: /posts/2025/08/11/new-tetra-radio-encryption-flaws-expose-law-enforcement-communications/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques découvertes dans le protocole de communication TETRA

Des chercheurs en cybersécurité ont identifié plusieurs failles majeures affectant le protocole TETRA, utilisé notamment par les forces de l'ordre et les infrastructures critiques. Ces vulnérabilités exposent les communications chiffrées à des attaques par rejeu, par force brute et permettent même le déchiffrement de flux.

**Points Clés :**

*   Le protocole TETRA, conçu pour les communications mobiles professionnelles, utilise plusieurs algorithmes de chiffrement (TEA1, TEA2, TEA3, TEA4).
*   Ces nouvelles découvertes font suite à des vulnérabilités antérieures trouvées en 2023.
*   Certaines failles sont liées à une implémentation affaiblie de l'AES-128 et à l'absence de protection contre le rejeu pour les messages SDS (Short Data Service).
*   Des vulnérabilités spécifiques ont également été trouvées dans certains terminaux TETRA Sepura, permettant l'exécution de code à distance.

**Vulnérabilités identifiées :**

*   **CVE-2025-52940 :** Vulnérabilité aux attaques par rejeu des flux vocaux chiffrés et injection de flux vocaux arbitraires.
*   **CVE-2025-52941 :** Utilisation d'une implémentation AES-128 affaiblie (56 bits d'entropie) rendant le chiffrement vulnérable aux attaques par force brute.
*   **CVE-2025-52942 :** Absence de protection contre le rejeu pour les messages SDS chiffrés.
*   **CVE-2025-52943 :** Risque de récupération de clés sur les réseaux supportant plusieurs algorithmes de chiffrement, permettant le déchiffrement ou l'injection de trafic TEA2/TEA3 via une clé TEA1 compromise.
*   **CVE-2025-52944 :** Absence d'authentification des messages, permettant l'injection de flux vocaux et de données arbitraires.
*   **MBPH-2025-001 (pas de CVE) :** Correction inefficace du CVE-2022-24401 contre les attaques de récupération de keystream.
*   **CVE-2025-52945 (Sepura) :** Restrictions défectueuses de gestion de fichiers sur les terminaux.
*   **CVE-2025-8458 (Sepura) :** Insuffisance d'entropie de clé pour le chiffrement de la carte SD sur les terminaux.
*   **MBPH-2025-003 (pas de CVE, Sepura) :** Exfiltration de la quasi-totalité du matériel de clé TETRA.

**Recommandations :**

*   Migrer vers des solutions de chiffrement de bout en bout (E2EE) plus robustes et auditées pour les flux vocaux et les messages SDS.
*   Utiliser des variantes E2EE non affaiblies pour le chiffrement AES-128.
*   Désactiver le support de l'algorithme TEA1 et faire pivoter toutes les clés Air Interface Encryption (AIE) sur les réseaux multi-algorithmes.
*   Pour l'utilisation de TETRA dans des applications de transport de données, ajouter une couche de sécurité supplémentaire comme TLS/VPN.
*   Pour les terminaux Sepura affectés, des correctifs sont attendus, mais une vulnérabilité architecturale empêche la remédiation complète de l'exfiltration des clés. Il est conseillé de renforcer les politiques de gestion des clés TETRA.

---
[Source](https://thehackernews.com/2025/08/new-tetra-radio-encryption-flaws-expose.html){:target="_blank"}
