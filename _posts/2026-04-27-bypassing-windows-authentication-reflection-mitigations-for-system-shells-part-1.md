---
title: 'Bypassing Windows authentication reflection mitigations for SYSTEM shells - Part 1'
date: 2026-04-27
permalink: /posts/2026/04/27/bypassing-windows-authentication-reflection-mitigations-for-system-shells-part-1/
tags:
- veille-cyber
- zerodaysfans
---
### Contournement de la réflexion d'authentification Windows (CVE-2025-33073 & CVE-2026-24294)

L'article analyse les vulnérabilités de réflexion d'authentification sur Windows, initialement corrigées par Microsoft dans le cadre de la **CVE-2025-33073**. Cette vulnérabilité exploitait une technique appelée « CMTI » (CredMarshalTargetInfo) pour forcer des services privilégiés (comme LSASS) à s'authentifier auprès d'un serveur contrôlé, permettant ensuite de relayer cette authentification localement pour obtenir des privilèges `NT AUTHORITY\SYSTEM`.

Le correctif initial de Microsoft se limitant à filtrer les noms de cibles SMB contenant des données malformées, les chercheurs ont démontré qu'il était possible de contourner cette protection en exploitant une nouvelle fonctionnalité introduite dans Windows 11 (24H2) et Windows Server 2025 : la possibilité de spécifier un port TCP arbitraire pour les connexions SMB.

#### Points clés
*   **Multiplexage SMB** : Le protocole SMB permet de multiplexer plusieurs sessions authentifiées sur une seule et même connexion TCP.
*   **Méthodologie de contournement** : Les chercheurs ont utilisé une approche itérative consistant à isoler les mécanismes non couverts par le correctif (protocoles autres que SMB, nouvelles fonctionnalités système) pour forcer une authentification locale.
*   **Exploitation du port arbitraire** : En forçant une connexion SMB sur un port personnalisé, un attaquant peut maintenir une connexion active et y injecter ultérieurement l'authentification d'un service privilégié coercé (via des outils comme PetitPotam), qui est ensuite relayée localement.

#### Vulnérabilités
*   **CVE-2025-33073** : Vulnérabilité initiale de réflexion d'authentification (CMTI).
*   **CVE-2026-24294** : Élévation de privilèges locale (LPE) via l'abus de la connexion SMB sur port arbitraire.

#### Recommandations
*   **Durcissement (Hardening)** : Appliquer les mises à jour de sécurité cumulatives de Microsoft (Patch Tuesday).
*   **Signature SMB** : L'activation obligatoire de la signature SMB (SMB Signing) atténue cette attaque, comme constaté sur Windows 11 24H2 où l'exploit ne fonctionne pas par défaut contrairement à Windows Server 2025.
*   **Surveillance** : Porter une attention particulière aux connexions SMB sortantes inhabituelles ou initiées vers des ports non standards par des processus système.

---
[Source](https://www.synacktiv.com/en/publications/bypassing-windows-authentication-reflection-mitigations-for-system-shells-part-1){:target="_blank"}
