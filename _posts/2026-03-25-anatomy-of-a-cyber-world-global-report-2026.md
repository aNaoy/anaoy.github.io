---
title: 'Anatomy of a Cyber World Global Report 2026'
date: 2026-03-25
permalink: /posts/2026/03/25/anatomy-of-a-cyber-world-global-report-2026/
tags:
- veille-cyber
- securelist
---
### Rapport mondial 2026 : Analyse du paysage des cybermenaces

Le rapport mondial 2026 de Kaspersky synthétise les données issues de ses services de détection et réponse managées (MDR), de réponse aux incidents (IR), d'évaluation des compromissions et de conseil SOC. En 2025, l'infrastructure MDR a traité en moyenne 15 000 événements de télémétrie par hôte par jour, générant 400 000 alertes, dont 39 000 ont nécessité une investigation humaine après filtrage.

**Points clés :**
*   **Secteurs ciblés :** Le gouvernement et l'industrie restent les cibles principales des incidents majeurs, tandis que le secteur IT a connu une hausse significative des demandes d'intervention, dépassant le secteur financier.
*   **Évolution des vecteurs d'attaque :** Plus de 80 % des attaques reposent désormais sur trois vecteurs initiaux : l'exploitation d'applications publiques, l'utilisation de comptes valides et les attaques par relations de confiance (en augmentation à 15,5 %).
*   **Techniques "Living-off-the-Land" (LotL) :** Les attaquants privilégient massivement les utilitaires Windows légitimes pour éviter la détection. Les outils les plus fréquemment observés sont `powershell.exe`, `rundll32.exe`, `mshta.exe`, ainsi que des logiciels tels que Mimikatz, PsExec et AnyDesk.
*   **Incidents de haute sévérité :** Bien qu'en baisse depuis 2021, ces incidents sont majoritairement le fait d'acteurs APT ou liés à des exercices de "red teaming".

**Vulnérabilités :**
*   Les produits Microsoft sont les plus exploités. 
*   La moitié des CVE identifiées permettent une exécution de code à distance (RCE), incluant des cas sans authentification préalable. (Note : Le rapport mentionne la tendance globale sans lister les identifiants CVE spécifiques dans le texte source).

**Recommandations :**
*   Renforcer la surveillance des accès aux applications exposées sur Internet.
*   Sécuriser davantage les relations de confiance avec les partenaires tiers pour prévenir les attaques en chaîne.
*   Mettre en place une stratégie de détection comportementale pour identifier l'usage détourné d'outils d'administration légitimes (PowerShell, PsExec, etc.).
*   Prioriser la remédiation des vulnérabilités RCE affectant l'infrastructure critique et les systèmes exposés.

---
[Source](https://securelist.com/global-report-security-services-2026/119233/){:target="_blank"}
