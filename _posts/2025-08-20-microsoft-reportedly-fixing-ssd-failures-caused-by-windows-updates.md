---
title: 'Microsoft reportedly fixing SSD failures caused by Windows updates'
date: 2025-08-20
permalink: /posts/2025/08/20/microsoft-reportedly-fixing-ssd-failures-caused-by-windows-updates/
tags:
- veille-cyber
- bleepingcomp
---
**Mise à jour Windows 11 : Risques pour les SSD**

Des mises à jour récentes de Windows 11, spécifiquement les KB5063878 et KB5062660, seraient à l'origine de problèmes de corruption de données et de défaillances affectant certains modèles de SSD et HDD. Les symptômes incluent la disparition des lecteurs du système d'exploitation lors d'opérations d'écriture intensives, notamment sur des disques dotés de contrôleurs Phison NAND. Certains utilisateurs ont signalé que ces problèmes surviennent après une utilisation du disque d'environ 60% et des écritures continues d'environ 50 Go. Les modèles sans DRAM de Phison sembleraient être plus sensibles. Des marques comme SanDisk, Corsair, KIOXIA et d'autres utilisant des contrôleurs Phison PS5012-E12 et InnoGrit sont potentiellement concernées.

Phison a confirmé travailler conjointement avec Microsoft pour résoudre ce problème. Microsoft n'a pas encore officiellement commenté ces rapports.

**Points clés :**

*   Des mises à jour récentes de Windows 11 provoquent des problèmes avec certains SSD et HDD.
*   Les symptômes concernent la corruption de données et l'inaccessibilité des lecteurs lors d'écritures importantes.
*   Les contrôleurs Phison NAND et les modèles sans DRAM semblent particulièrement affectés.

**Vulnérabilités :**

*   Aucune CVE n'est mentionnée dans l'article.

**Recommandations :**

*   Éviter l'écriture de fichiers volumineux (plusieurs dizaines de Go) ou de multiples fichiers volumineux en succession rapide. Privilégier des écritures par lots plus petits étalées dans le temps.
*   Extraire des fichiers compressés volumineux en plusieurs étapes plutôt qu'en une seule fois.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-reportedly-fixing-ssd-failures-caused-by-windows-updates/){:target="_blank"}
