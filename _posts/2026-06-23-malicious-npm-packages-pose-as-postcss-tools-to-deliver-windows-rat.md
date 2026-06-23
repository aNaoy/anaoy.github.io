---
title: 'Malicious npm Packages Pose as PostCSS Tools to Deliver Windows RAT'
date: 2026-06-23
permalink: /posts/2026/06/23/malicious-npm-packages-pose-as-postcss-tools-to-deliver-windows-rat/
tags:
- veille-cyber
- hackernews
---
### Propagation de RAT Windows via des paquets npm malveillants

Des chercheurs ont identifié plusieurs paquets npm malveillants, notamment `aes-decode-runner-pro`, `postcss-minify-selector` et `postcss-minify-selector-parser`, usurpant l'identité d'outils légitimes pour déployer un cheval de Troie d'accès à distance (RAT) sur Windows. Cette campagne s'inscrit dans une recrudescence d'attaques sur la chaîne d'approvisionnement logicielle visant les environnements de développement.

**Points clés :**
* **Méthode d'infection :** Les paquets contiennent un script JavaScript qui exécute PowerShell pour télécharger une archive ZIP depuis un serveur distant (`nvidiadriver[.]net`).
* **Charge utile :** L'archive contient un environnement Python compilé (via Nuitka) permettant au malware de collecter des informations système, d'exfiltrer des identifiants (Google Chrome, extensions), d'exécuter des commandes shell et de transférer des fichiers vers un serveur C2 (`95.216.92[.]207:8080`).
* **Contournement :** Le malware utilise des modules Python spécialisés, dont `auto.pyd`, capable de contourner les protections de chiffrement "App-Bound" (ABE) de Chrome.
* **Contexte élargi :** Plusieurs autres campagnes simultanées ciblent l'écosystème npm avec des outils de vol d'identifiants (ex: `@withgoogle/stitch-sdk`) ou des RAT avancés (ex: `apintergrationpost`).

**Vulnérabilités :**
Aucune CVE spécifique n'est associée, l'attaque exploitant le mécanisme de confiance des dépendances logicielles (typosquatting et usurpation d'outils de build populaires).

**Recommandations :**
* **Suppression immédiate :** Désinstaller tout paquet suspect et supprimer les fichiers créés par ceux-ci sur les machines infectées.
* **Rotation des accès :** Réinitialiser systématiquement tous les identifiants et clés d'API présents sur les postes de développement ayant utilisé ces dépendances.
* **Vigilance accrue :** Traiter les nouveaux paquets ou les dépendances de build peu connues avec méfiance, même lorsqu'elles imitent des bibliothèques légitimes.
* **Audit des dépendances :** Mettre en place des outils d'analyse de la chaîne d'approvisionnement pour détecter les paquets malveillants ou suspects avant leur intégration dans les projets.

---
[Source](https://thehackernews.com/2026/06/malicious-npm-packages-pose-as-postcss.html){:target="_blank"}
