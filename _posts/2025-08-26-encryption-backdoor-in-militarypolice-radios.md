---
title: 'Encryption Backdoor in Military/Police Radios'
date: 2025-08-26
permalink: /posts/2025/08/26/encryption-backdoor-in-militarypolice-radios/
tags:
- veille-cyber
- schneier
---
**Vulnérabilités critiques dans les communications radio militaires et policières**

Des chercheurs en sécurité ont découvert plusieurs failles dans le standard radio européen TETRA, utilisé par des fabricants majeurs comme Motorola, Damm et Sepura depuis les années 90. Initialement, ces vulnérabilités étaient cachées par le caractère propriétaire des algorithmes de chiffrement.

Les recherches récentes ont mis en évidence une implémentation du chiffrement de bout en bout (E2EE) au sein de ce standard, qui réduit une clé de chiffrement de 128 bits à seulement 56 bits. Cette compression affaiblit considérablement la sécurité, rendant le trafic potentiellement facile à intercepter. L'identification exacte des utilisateurs de cette implémentation d'E2EE et leur niveau de connaissance de cette faille restent inconnus. Les chercheurs suggèrent que ces faiblesses pourraient être des portes dérobées intentionnellement introduites.

**Points clés :**

*   Découverte de vulnérabilités dans le standard radio européen TETRA.
*   Les failles affectent les communications chiffrées utilisées par les forces militaires et policières.
*   Une implémentation spécifique du chiffrement de bout en bout présente une réduction de clé qui affaiblit le chiffrement.
*   Possibilité de portes dérobées intentionnellement implantées.

**Vulnérabilités :**

*   Plusieurs vulnérabilités dans le standard TETRA.
*   Dans une implémentation E2EE : réduction d'une clé de 128 bits à 56 bits avant le chiffrement. (Pas de CVE spécifié dans l'article).

**Recommandations :**

*   (Non explicitement mentionnées, mais implicitement la nécessité d'examiner et de sécuriser les implémentations de chiffrement.)

---
[Source](https://www.schneier.com/blog/archives/2025/08/encryption-backdoor-in-military-police-radios.html){:target="_blank"}
