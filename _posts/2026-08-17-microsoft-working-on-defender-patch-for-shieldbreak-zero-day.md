---
title: 'Microsoft working on Defender patch for ShieldBreak zero-day'
date: 2026-08-17
permalink: /posts/2026/08/17/microsoft-working-on-defender-patch-for-shieldbreak-zero-day/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilité "ShieldBreak" dans Microsoft Defender : Une escalade de privilèges critique

Microsoft développe actuellement un correctif pour « ShieldBreak », une vulnérabilité zero-day de type escalade de privilèges affectant le moteur de protection de Microsoft Defender. Cette faille permet à un attaquant disposant d'un accès local limité d'obtenir des privilèges **SYSTEM** sur Windows 10, Windows 11 et Windows Server.

**Points clés :**
*   **Origine :** La faille a été découverte par le chercheur "Nightmare Eclipse". Elle constitue un contournement effectif du correctif précédent lié à la vulnérabilité *RoguePlanet*.
*   **Portée :** Le proof-of-concept (PoC) affiche un taux de réussite de 100 % sur les versions récentes de Windows 11 et Windows Server 2025.
*   **Contexte :** Le chercheur a rendu public cet exploit sans préavis, suite à un désaccord persistant avec Microsoft concernant ses politiques de divulgation et ses programmes de primes aux bugs (bug bounty).
*   **Réponse de Microsoft :** La firme a confirmé enquêter sur le problème et travaille sur un correctif, tout en ayant précédemment mis en garde contre les activités de divulgation qu'elle juge malveillantes.

**Vulnérabilité identifiée :**
*   **CVE-2026-69414** : Escalade de privilèges dans le moteur de protection contre les programmes malveillants de Microsoft Defender.

**Recommandations :**
*   **Surveillance :** Étant donné qu'aucun correctif n'est encore disponible, il est conseillé de surveiller les annonces de sécurité de Microsoft via le [guide des mises à jour MSRC](https://msrc.microsoft.com/update-guide/).
*   **Application des correctifs :** Dès que le patch officiel sera publié, il est impératif de l'appliquer immédiatement sur l'ensemble des systèmes Windows (postes de travail et serveurs) sur lesquels Microsoft Defender est actif.

---
[Source](https://www.bleepingcomputer.com/news/security/microsoft-working-on-defender-patch-for-shieldbreak-zero-day/){:target="_blank"}
