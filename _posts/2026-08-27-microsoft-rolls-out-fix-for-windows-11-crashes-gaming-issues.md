---
title: 'Microsoft rolls out fix for Windows 11 crashes, gaming issues'
date: 2026-08-27
permalink: /posts/2026/08/27/microsoft-rolls-out-fix-for-windows-11-crashes-gaming-issues/
tags:
- veille-cyber
- bleepingcomp
---
### Correction du bug de plantage des jeux sur Windows 11 lié aux périphériques RGB

Microsoft a déployé un correctif pour résoudre des instabilités et des plantages système (erreurs `EXCEPTION_ACCESS_VIOLATION`) affectant les utilisateurs de Windows 11 (versions 24H2 et 25H2).

**Points clés :**
*   **Cause identifiée :** Le problème est provoqué par le pilote `inpoutx64.sys`, associé à certains composants ou périphériques dotés d'un éclairage RGB.
*   **Mécanisme :** Le pilote entre en conflit avec le lancement de certains jeux, tels que *ARC Raiders*, *MARVEL Tōkon: Fighting Souls* et *The Finals*.
*   **Solution automatique :** Microsoft déploie un blocage du pilote `inpoutx64.sys` via une mise à jour automatique. Le système affiche une notification lors de la désactivation, puis le jeu peut fonctionner normalement après un redémarrage.

**Vulnérabilités :**
*   Aucune CVE n'est associée à cet incident, il s'agit d'une incompatibilité logicielle liée à un pilote spécifique.

**Recommandations :**
*   **Utilisateurs grand public :** Laissez les mises à jour automatiques s'installer. Le correctif est en cours de propagation et sera intégré aux mises à jour de sécurité de septembre 2026.
*   **Administrateurs informatiques (systèmes gérés) :** Pour les parcs où la mise à jour ne se déploie pas automatiquement, désactivez manuellement le pilote via le Registre Windows :
    1. Accédez à `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\inpoutx64`.
    2. Modifiez la valeur de la clé **Start** à `4`.
    3. Redémarrez l'ordinateur (une sauvegarde préalable du Registre est fortement recommandée).

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-rolls-out-fix-for-windows-11-crashes-gaming-issues/){:target="_blank"}
