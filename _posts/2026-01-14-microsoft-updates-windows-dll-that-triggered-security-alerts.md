---
title: 'Microsoft updates Windows DLL that triggered security alerts'
date: 2026-01-14
permalink: /posts/2026/01/14/microsoft-updates-windows-dll-that-triggered-security-alerts/
tags:
- veille-cyber
- bleepingcomp
---
### Faux positifs de sécurité dans Windows résolus

Microsoft a corrigé un problème où certaines applications de sécurité signalaient à tort un composant essentiel de Windows, WinSqlite3.dll, comme étant vulnérable. Cette bibliothèque dynamique (DLL) implémente le moteur de base de données SQLite et est incluse dans les installations de Windows. Les alertes de sécurité provenaient d'une détection erronée d'une vulnérabilité de corruption de mémoire, identifiée par CVE-2025-6965.

Le problème a affecté une large gamme de plateformes Windows, y compris les versions clients (Windows 10, Windows 11) et serveurs (Windows Server 2012 à 2025).

Microsoft a confirmé le problème et a publié des mises à jour pour WinSqlite3.dll via les mises à jour Windows de juin 2025 et ultérieures, puis résolu définitivement le problème dans les mises à jour du 13 janvier 2026 et plus récentes. Il est recommandé d'installer la dernière mise à jour disponible pour les systèmes concernés.

Il est important de noter que WinSqlite3.dll est distinct de sqlite3.dll, qui n'est pas un composant de Windows.

**Points clés :**

*   Des applications de sécurité ont faussement signalé la DLL WinSqlite3.dll comme vulnérable.
*   La vulnérabilité citée était liée à une corruption de mémoire (CVE-2025-6965).
*   Le problème a affecté un grand nombre de systèmes d'exploitation Windows.
*   Microsoft a corrigé le problème via des mises à jour Windows.

**Vulnérabilités :**

*   CVE-2025-6965 (Fausse détection liée à une corruption de mémoire)

**Recommandations :**

*   Installer les mises à jour Windows les plus récentes pour inclure les correctifs de sécurité et les résolutions de problèmes.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-updates-windows-dll-that-triggered-security-alerts/){:target="_blank"}
