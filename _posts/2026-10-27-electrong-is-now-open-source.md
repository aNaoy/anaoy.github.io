---
title: 'ElectroNG is now open source!'
date: 2026-10-27
permalink: /posts/2026/10/27/electrong-is-now-open-source/
tags:
- veille-cyber
- zerodaysfans
---
### Libération d'ElectroNG : Vers une sécurité collaborative pour Electron

Doyensec a rendu **ElectroNG** open source sous licence Apache 2.0. Ce projet, qui succède à l'outil *Electronegativity* (désormais archivé), est un scanner d'analyse statique (SAST) conçu spécifiquement pour identifier les vulnérabilités et les mauvaises configurations dans les applications basées sur Electron. Le code a été scindé en deux dépôts : l'interface graphique (**ElectroNG**) et le moteur d'analyse (**ElectroNG-core**).

**Points clés :**
* **Évolution :** Contrairement à son prédécesseur en ligne de commande, ElectroNG offre une interface graphique permettant la gestion de projets, le tri des résultats (faux positifs, ajustement de sévérité) et l'exportation de rapports (PDF, HTML, XLSX, CSV, SARIF).
* **Capacités :** Le moteur intègre environ 60 règles de sécurité, une base de données répertoriant plus de 650 vulnérabilités connues liées à Electron et des fonctions d'audit pour `BrowserWindow` et `BrowserView`.
* **État actuel :** Le développement actif a cessé en 2024. L'outil nécessite des mises à jour pour supporter les versions les plus récentes d'Electron et réduire le taux de "bruit" (faux positifs).

**Vulnérabilités couvertes :**
L'outil se concentre sur les anti-patrons de sécurité spécifiques à Electron, notamment :
* Mauvaises configurations des options de `webPreferences` (ex: `nodeIntegration`, `contextIsolation`).
* Mauvaises pratiques dans le chargement des ressources distantes ou locales.
* Utilisation de versions d'Electron obsolètes présentant des vulnérabilités connues (CVE).

**Recommandations pour la communauté :**
Doyensec encourage les contributions pour pérenniser l'outil, en se focalisant sur :
* **Modernisation :** Mise à jour des dépendances et du processus de build.
* **Détection :** Amélioration de l'analyse JS/TS et ajout de nouvelles règles de détection.
* **Fiabilité :** Ajout de tests de régression pour valider la précision des résultats.
* **Couverture :** Alignement des vérifications avec les APIs et standards de sécurité actuels d'Electron.

---
[Source](https://blog.doyensec.com/2026/10/27/electrong-oss.html){:target="_blank"}
