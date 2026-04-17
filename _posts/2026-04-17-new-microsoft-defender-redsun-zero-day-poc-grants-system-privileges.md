---
title: 'New Microsoft Defender “RedSun” zero-day PoC grants SYSTEM privileges'
date: 2026-04-17
permalink: /posts/2026/04/17/new-microsoft-defender-redsun-zero-day-poc-grants-system-privileges/
tags:
- veille-cyber
- bleepingcomp
---
### "RedSun" : Une faille zero-day critique dans Microsoft Defender

Un chercheur en cybersécurité, sous le pseudonyme « Chaotic Eclipse », a publié une preuve de concept (PoC) exploitant une vulnérabilité zero-day nommée « RedSun » au sein de Microsoft Defender. Cette faille permet à un utilisateur local d'élever ses privilèges jusqu'au niveau **SYSTEM** sur Windows 10, Windows 11 et Windows Server.

**Points clés :**
*   **Mécanisme d'exploitation :** L'exploit abuse de la fonction de réécriture de fichiers de Microsoft Defender. Lorsqu'un fichier malveillant est identifié, Defender tente de le réécrire, ce qui est détourné via l'API *Cloud Files* et des points de jonction pour remplacer un binaire système (`TieringEngineService.exe`) par un code malveillant.
*   **Motivation :** La publication de cette vulnérabilité est un acte de protestation contre les pratiques de gestion des chercheurs en sécurité par le centre de réponse de Microsoft (MSRC).
*   **Impact :** La faille est confirmée comme étant fonctionnelle sur des systèmes Windows entièrement mis à jour, rendant les mesures de sécurité actuelles inopérantes face à cette attaque.

**Vulnérabilités :**
*   **Type :** Élévation locale de privilèges (LPE).
*   **CVE :** Aucune CVE attribuée pour le moment (le dossier est en cours d'analyse suite à la divulgation publique).

**Recommandations :**
*   **Vigilance accrue :** Dans l'attente d'un correctif officiel de Microsoft, il est crucial de restreindre l'accès local aux machines.
*   **Surveillance :** Les équipes de sécurité doivent surveiller les activités suspectes impliquant le service `TieringEngineService.exe` ou des modifications anormales dans les dossiers système via des outils de détection d'EDR.
*   **Stratégie de défense :** Appliquer le principe du moindre privilège pour les utilisateurs locaux afin de limiter l'impact potentiel d'une exploitation réussie de cette faille.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/new-microsoft-defender-redsun-zero-day-poc-grants-system-privileges/){:target="_blank"}
