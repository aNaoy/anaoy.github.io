---
title: 'QNAP warns of critical ASP.NET flaw in its Windows backup software'
date: 2025-10-28
permalink: /posts/2025/10/28/qnap-warns-of-critical-aspnet-flaw-in-its-windows-backup-software/
tags:
- veille-cyber
- bleepingcomp
---
**Vulnérabilité critique dans le logiciel de sauvegarde QNAP**

Une faille de sécurité majeure affecte le logiciel NetBak PC Agent de QNAP, un utilitaire Windows utilisé pour sauvegarder des données sur des périphériques de stockage en réseau (NAS). Cette vulnérabilité, identifiée sous la référence CVE-2025-55315, réside dans le serveur web ASP.NET Core Kestrel.

Elle permet à des attaquants peu privilégiés de voler les identifiants d'autres utilisateurs ou de contourner les contrôles de sécurité frontaux grâce à une technique appelée HTTP request smuggling. L'exploitation réussie pourrait mener à une prise d'identité d'un autre utilisateur, à la contournement des protections contre le CSRF, ou à des injections.

**Points Clés :**

*   **Composant affecté :** NetBak PC Agent de QNAP (logiciel de sauvegarde pour Windows).
*   **Cause racine :** Une vulnérabilité dans ASP.NET Core Kestrel (CVE-2025-55315).
*   **Type de vulnérabilité :** Contournement de sécurité via HTTP request smuggling.
*   **Conséquences potentielles :** Vol d'identifiants, élévation de privilèges, contournement de sécurité, accès non autorisé à des données sensibles, modification de fichiers serveur, et conditions de déni de service limité.

**Recommandations :**

*   Les utilisateurs de QNAP sont fortement encouragés à installer les dernières mises à jour de sécurité pour ASP.NET Core sur leurs systèmes Windows.
*   Pour sécuriser leurs systèmes, les utilisateurs doivent soit réinstaller l'application NetBak PC Agent pour obtenir les derniers composants ASP.NET Core, soit mettre à jour manuellement ASP.NET Core sur leurs PC en téléchargeant et installant le dernier "ASP.NET Core Runtime (Hosting Bundle)" depuis la page de téléchargement de .NET 8.0.

---
[Source](https://www.bleepingcomputer.com/news/security/qnap-warns-its-windows-backup-software-is-also-affected-by-critical-aspnet-flaw/){:target="_blank"}
