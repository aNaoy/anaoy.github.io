---
title: 'Microsoft working on Defender patch for RoguePlanet zero-day'
date: 2026-06-17
permalink: /posts/2026/06/17/microsoft-working-on-defender-patch-for-rogueplanet-zero-day/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilité "RoguePlanet" dans Microsoft Defender : Microsoft prépare un correctif

Microsoft a confirmé travailler sur un correctif pour une vulnérabilité « zero-day » critique affectant Microsoft Defender, baptisée **RoguePlanet**. Cette faille permet à un attaquant d'élever ses privilèges au niveau **SYSTEM** sur des systèmes Windows 10 et 11 entièrement à jour.

**Points clés :**
*   **Nature de la faille :** Il s'agit d'une condition de concurrence (*race condition*) au sein du moteur de protection contre les logiciels malveillants de Microsoft.
*   **Impact :** L'exploit fonctionne indépendamment de l'activation de la protection en temps réel, permettant l'ouverture d'invites de commande avec des privilèges administrateurs complets.
*   **Contexte :** La vulnérabilité a été divulguée publiquement par un chercheur en sécurité nommé « Nightmare Eclipse », dans le cadre d'un conflit persistant avec Microsoft concernant les politiques de divulgation et les programmes de récompense aux bugs (*bug bounty*).
*   **Historique :** Ce chercheur est à l'origine de plusieurs fuites récentes de zero-days visant divers composants Windows et Microsoft Defender, Microsoft ayant par ailleurs menacé d'engager des poursuites judiciaires contre les divulgations jugées malveillantes.

**Vulnérabilité identifiée :**
*   **CVE-2026-50656**

**Recommandations :**
*   **Surveillance :** Aucun correctif n'est disponible à ce jour. Les administrateurs systèmes doivent surveiller les annonces officielles de Microsoft et les bulletins de sécurité.
*   **Attente de mise à jour :** Il est fortement conseillé d'appliquer le correctif dès sa publication via Windows Update pour corriger cette faille d'élévation de privilèges.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-working-on-defender-patch-for-rogueplanet-zero-day/){:target="_blank"}
