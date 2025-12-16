---
title: 'Microsoft to block Exchange Online access for outdated mobile devices'
date: 2025-12-16
permalink: /posts/2025/12/16/microsoft-to-block-exchange-online-access-for-outdated-mobile-devices/
tags:
- veille-cyber
- bleepingcomp
---
**Fin de support pour les anciens appareils mobiles sur Exchange Online**

À compter du 1er mars 2026, Microsoft bloquera l'accès à Exchange Online pour les appareils mobiles utilisant des versions antérieures à 16.1 du protocole Exchange ActiveSync (EAS). Cette mesure vise à renforcer la sécurité et la fiabilité du service de messagerie cloud de Microsoft.

**Points clés :**

*   Les appareils utilisant des applications natives de messagerie et se connectant à Exchange Online sont concernés.
*   Les appareils utilisant l'application Outlook Mobile ne sont pas affectés, car elle n'utilise pas EAS.
*   Les installations d'Exchange Server locales ne sont pas impactées.
*   La version EAS 16.1 a été introduite en juin 2016. Les iPhones sous iOS 10 et versions ultérieures sont compatibles, tout comme les applications de messagerie Android qui seront mises à jour par Google et Samsung.

**Vulnérabilités :**

Bien que l'article ne mentionne pas de CVE spécifiques associées directement à cette décision, le fait de bloquer les anciennes versions d'EAS implique que ces versions peuvent présenter des failles de sécurité non corrigées, rendant les appareils vulnérables aux menaces.

**Recommandations :**

*   Les utilisateurs et les organisations doivent s'assurer que leurs appareils mobiles et leurs applications de messagerie sont à jour avant le 1er mars 2026.
*   Les administrateurs IT peuvent utiliser la commande PowerShell fournie (`Get-MobileDevice | Where-Object {($_.ClientType -eq 'EAS' -or $_.ClientType -match 'ActiveSync') -and $_.ClientVersion -and ([version]$_.ClientVersion -lt [version]'16.1')} | Sort-Object UserDisplayName | Select-Object UserDisplayName, UserPrincipalName, DeviceId, DeviceModel`) pour identifier les appareils utilisant des versions EAS obsolètes dans leur organisation.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-to-block-exchange-online-access-for-outdated-mobile-devices/){:target="_blank"}
