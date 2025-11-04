---
title: 'Microsoft removing Defender Application Guard from Office'
date: 2025-11-04
permalink: /posts/2025/11/04/microsoft-removing-defender-application-guard-from-office/
tags:
- veille-cyber
- bleepingcomp
---
**Fin de Microsoft Defender Application Guard pour Office**

Microsoft retire progressivement Microsoft Defender Application Guard (MDAG) pour Office, une fonctionnalité conçue pour isoler les fichiers Word, PowerPoint et Excel non fiables dans un conteneur sécurisé afin de protéger le système d'exploitation hôte. Ce retrait débutera en février 2026 avec la version 2602 d'Office et sera finalisé en décembre 2027 avec la version 2612.

Dorénavant, les fichiers Office s'ouvriront en "Vue Protégée", un mode lecture seule qui limite les fonctionnalités d'édition.

**Points Clés :**

*   **Suppression progressive :** MDAG pour Office sera retiré entre février 2026 et décembre 2027.
*   **Remplacement :** Les fichiers s'ouvriront automatiquement en "Vue Protégée".
*   **Alternatives recommandées :** Microsoft propose d'activer les règles de réduction de la surface d'attaque de Microsoft Defender pour Endpoint et le Contrôle d'Application Windows Defender.

**Vulnérabilités :**

Aucune vulnérabilité spécifique (CVE) n'est mentionnée dans l'article concernant le retrait de MDAG. Le retrait est présenté comme une évolution de la stratégie de sécurité de Microsoft.

**Recommandations :**

Pour maintenir la sécurité contre les documents Office malveillants, il est recommandé aux administrateurs :

*   D'activer les règles de réduction de la surface d'attaque (ASR) de Microsoft Defender pour Endpoint.
*   D'activer le Contrôle d'Application Windows Defender (WDAC) pour garantir l'exécution uniquement du code de confiance.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-removing-defender-application-guard-from-office/){:target="_blank"}
