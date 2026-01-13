---
title: 'Windows 11 KB5074109 & KB5073455 cumulative updates released'
date: 2026-01-13
permalink: /posts/2026/01/13/windows-11-kb5074109-kb5073455-cumulative-updates-released/
tags:
- veille-cyber
- bleepingcomp
---
**Mises à jour Cumulatives pour Windows 11 : Janvier 2026**

Microsoft a déployé des mises à jour cumulatives, KB5074109 et KB5073455, pour les versions 25H2/24H2 et 23H2 de Windows 11. Ces mises à jour, considérées comme obligatoires, intègrent les correctifs de sécurité du "Patch Tuesday" de janvier 2026, visant à résoudre des vulnérabilités découvertes précédemment. Elles corrigent également des bugs et introduisent de nouvelles fonctionnalités. Les utilisateurs peuvent installer ces mises à jour via Windows Update ou en les téléchargeant manuellement depuis le Microsoft Update Catalog.

**Points Clés :**

*   **Mises à Jour Obligatoires :** Ces mises à jour incluent les correctifs de sécurité essentiels de janvier 2026.
*   **Versions Concernées :** Windows 11 versions 25H2/24H2 (KB5074109) et 23H2 (KB5073455).
*   **Fixes de Bugs :** Résolution de plusieurs problèmes, notamment ceux affectant les réseaux sous-système Linux (WSL), les connexions RemoteApp dans Azure Virtual Desktop, la consommation d'énergie des appareils avec NPU, et la détection erronée de vulnérabilités pour le composant WinSqlite3.dll.
*   **Nouvelles Fonctionnalités :** Introduction d'un processus de déploiement progressif pour les certificats Secure Boot afin d'améliorer la sécurité.
*   **Changements de Comportement :** Les pilotes modem agrsm64.sys, agrsm.sys, smserl64.sys et smserial.sys sont supprimés, rendant le matériel modem dépendant de ces pilotes inopérant. Les Services de déploiement Windows (WDS) ne supporteront plus la fonctionnalité de déploiement mains libres par défaut.
*   **Problèmes Connus :** Microsoft n'a signalé aucun nouveau problème généralisé, à l'exception d'un bug qui masque le bouton permettant de rendre visible le champ du mot de passe.

**Vulnérabilités :**

L'article mentionne que ces mises à jour corrigent des "vulnérabilités découvertes dans les mois précédents" et intègrent des "correctifs de sécurité". Aucune vulnérabilité spécifique avec un identifiant CVE n'est détaillée dans ce texte.

**Recommandations :**

*   Installer immédiatement les mises à jour KB5074109 et KB5073455 via Windows Update.
*   Pour les utilisateurs avancés, le téléchargement et l'installation manuelle depuis le Microsoft Update Catalog sont une option.
*   Les administrateurs systèmes doivent consulter la documentation sur le durcissement du déploiement mains libres des Services de déploiement Windows (WDS) pour s'adapter au changement de comportement.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/windows-11-kb5074109-and-kb5073455-cumulative-updates-released/){:target="_blank"}
