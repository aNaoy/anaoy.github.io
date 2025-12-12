---
title: 'Malicious VSCode Marketplace extensions hid trojan in fake PNG file'
date: 2025-12-12
permalink: /posts/2025/12/12/malicious-vscode-marketplace-extensions-hid-trojan-in-fake-png-file/
tags:
- veille-cyber
- bleepingcomp
---
### Extensions VSCode Compromises : Un Cheval de Troie Masqué

Une campagne malveillante a été découverte impliquant 19 extensions du VSCode Marketplace, actives depuis février. Ces extensions ciblent les développeurs en dissimulant un cheval de troie dans des dossiers de dépendances, pré-empaquetés pour éviter le téléchargement depuis le registre npm.

L'attaque exploite une dépendance modifiée, comme `path-is-absolute` ou `@actions/io`, intégrant du code malveillant exécuté au démarrage de VSCode. Ce code décode un chargeur JavaScript obfusqué et, à partir d'une archive camouflée en fichier `.PNG` (nommée `banner.png`), déploie un fichier binaire malveillant (`cmstp.exe` et un autre basé sur Rust). Les capacités complètes du trojan sont encore à l'étude.

Les extensions compromises, publiées sous la version 1.0.0, incluent des noms tels que "Malkolm Theme", "PandaExpress Theme", "Prada 555 Theme" et "Priskinski Theme". Bien qu'elles aient été retirées du marketplace par Microsoft, les utilisateurs ayant installé ces extensions sont invités à scanner leurs systèmes.

**Points Clés :**

*   19 extensions VSCode Marketplace compromises.
*   Malware caché dans des dépendances pré-empaquetées (`node_modules`).
*   Utilisation d'un fichier PNG frauduleux pour masquer des binaires malveillants.
*   Ciblage des développeurs via l'IDE VSCode.

**Vulnérabilités :**

*   Aucune CVE spécifique n'est mentionnée dans l'article. L'attaque repose sur l'insertion de code malveillant dans des dépendances légitimes et la dissimulation de binaires dans des fichiers apparemment innocents.

**Recommandations :**

*   Inspecter attentivement les extensions avant l'installation, particulièrement celles provenant d'éditeurs moins connus.
*   Vérifier le contenu des dépendances incluses dans les paquets, surtout si elles ne sont pas récupérées d'une source fiable comme npm.
*   Analyser les systèmes à la recherche de signes d'infection si des extensions suspectes ont été installées.

---
[Source](https://www.bleepingcomputer.com/news/security/malicious-vscode-marketplace-extensions-hid-trojan-in-fake-png-file/){:target="_blank"}
