---
title: 'New Microsoft Defender ShieldBreak zero-day grants SYSTEM privileges'
date: 2026-08-12
permalink: /posts/2026/08/12/new-microsoft-defender-shieldbreak-zero-day-grants-system-privileges/
tags:
- veille-cyber
- bleepingcomp
---
### La faille "ShieldBreak" expose les systèmes Windows à une élévation de privilèges

Le chercheur en sécurité "Nightmare Eclipse" a publié une nouvelle vulnérabilité zero-day baptisée **ShieldBreak**, ciblant Microsoft Defender. Cette faille permet d'obtenir des privilèges **SYSTEM** sur des systèmes Windows 10, 11 et Server entièrement mis à jour, en contournant le correctif précédent déployé pour la vulnérabilité *RoguePlanet*.

**Points clés :**
*   **Mécanisme :** ShieldBreak utilise un *callback hook* en mode utilisateur pour modifier le contenu des fichiers lors d'une analyse via l'API Cloud Filter (cfapi) de Microsoft Defender.
*   **Impact :** Élévation de privilèges locaux vers le niveau SYSTEM avec un taux de réussite de 100 % sur les versions testées.
*   **Contexte :** Cette divulgation s'inscrit dans un conflit tendu entre le chercheur et Microsoft concernant les politiques de divulgation et de récompenses (bug bounty), Microsoft ayant menacé de poursuites judiciaires suite à plusieurs fuites d'exploits.

**Vulnérabilités associées :**
*   **CVE-2026-50656 :** Identifiant de la faille *RoguePlanet* (le correctif est considéré comme incomplet par le chercheur).
*   **ShieldBreak :** Aucune CVE attribuée pour le moment, en attente de correctif.

**Recommandations :**
*   **Surveillance :** Les administrateurs peuvent utiliser les requêtes de détection publiées par l'expert en sécurité Kevin Beaumont (disponibles sur GitHub) pour identifier les tentatives d'exploitation de ShieldBreak dans *Microsoft Defender for Endpoint*.
*   **Veille :** Surveiller les bulletins de sécurité officiels de Microsoft pour le déploiement d'un correctif dédié. 
*   **Atténuation :** Bien qu'il soit difficile de neutraliser une telle faille sans correctif, le maintien d'une posture de défense en profondeur est essentiel, car l'exploitation nécessite que Microsoft Defender soit activé sur la machine cible.

---
[Source](https://www.bleepingcomputer.com/news/security/new-microsoft-defender-shieldbreak-zero-day-grants-system-privileges/){:target="_blank"}
