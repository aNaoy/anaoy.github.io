---
title: 'TEE.Fail attack breaks confidential computing on Intel, AMD, NVIDIA CPUs'
date: 2025-10-28
permalink: /posts/2025/10/28/teefail-attack-breaks-confidential-computing-on-intel-amd-nvidia-cpus/
tags:
- veille-cyber
- bleepingcomp
---
## TEE.Fail : Une Faille Critique dans les Environnements d'Exécution Sécurisés

Des chercheurs ont mis au jour une nouvelle attaque, nommée TEE.Fail, qui compromet la sécurité des environnements d'exécution de confiance (TEE) présents sur les processeurs Intel, AMD et NVIDIA. Ces TEE sont conçus pour isoler et protéger les données sensibles, tels que les clés cryptographiques, des autres parties du système, y compris le système d'exploitation.

L'attaque exploite une faiblesse au niveau du bus mémoire DDR5, permettant l'interception des données transmises. Contrairement à des attaques antérieures nécessitant une expertise poussée, TEE.Fail serait réalisable par des passionnés d'informatique pour un coût relativement modeste (moins de 1 000 $). Elle exige cependant un accès physique à la machine cible et des privilèges d'administrateur pour modifier le pilote du noyau.

En raison de compromis architecturaux liés à l'adoption de la mémoire DDR5 et de l'utilisation du chiffrement AES-XTS qui est déterministe, TEE.Fail permet de lire les données chiffrées transitant dans la mémoire. Les attaquants peuvent ainsi reconstruire des clés privées, usurper des identités numériques (attestation) et potentiellement compromettre la confidentialité totale des données traitées dans les TEE. Des démonstrations ont permis de falsifier des attestations pour accéder à des données confidentielles ou pour exécuter des charges de travail frauduleusement légitimes.

Les vendeurs concernés ont été informés et travaillent sur des correctifs.

### Points Clés :

*   **Nom de l'attaque :** TEE.Fail
*   **Cible :** Environnements d'Exécution de Confiance (TEE) sur processeurs Intel (SGX, TDX), AMD (SEV-SNP), et NVIDIA.
*   **Mécanisme :** Attaque par interposition sur le bus mémoire DDR5, exploitant le chiffrement déterministe AES-XTS.
*   **Conditions :** Accès physique à la machine et privilèges administrateur.
*   **Impact :** Extraction de secrets, falsification d'attestations, compromission de la confidentialité.

### Vulnérabilités :

Bien que l'article ne mentionne pas de CVEs spécifiques, les vulnérabilités exploitées sont liées à :

*   **Chiffrement mémoire DDR5 déterministe (AES-XTS) :** Permet de déduire le contenu à partir du ciphertext si l'adresse est connue.
*   **Architecture des TEE modernes :** Des compromis liés aux performances et à la scalabilité auraient affaibli les protections d'intégrité et de non-rejeu de la mémoire.
*   **Exposition des interfaces mémoire :** Intel a exposé une interface pour les adresses physiques à la composante de traduction d'adresses mémoire, facilitant l'identification des emplacements mémoire.

### Recommandations :

*   Les fabricants (Intel, AMD, NVIDIA) travaillent sur des **mitigations** pour contrer cette menace.
*   L'article souligne la nécessité de revoir le **modèle de menace** pour le calcul confidentiel.
*   Étant donné les exigences physiques de l'attaque, les utilisateurs individuels sont moins directement concernés que les infrastructures critiques et les centres de données.

---
[Source](https://www.bleepingcomputer.com/news/security/teefail-attack-breaks-confidential-computing-on-intel-amd-nvidia-cpus/){:target="_blank"}
