---
title: '⚡ Weekly Recap: N-able 0-Days, Windows 0-Days, Chrome 0-Days, Fridge 0-Days, and More Bad Days'
date: 2026-11-16
permalink: /posts/2026/11/16/weekly-recap-n-able-0-days-windows-0-days-chrome-0-days-fridge-0-days-and-more-bad-days/
tags:
- veille-cyber
- hackernews
---
### Actualités Cyber : 0-Days en série et automatisation des menaces

Cette semaine a été marquée par une vague d'exploits « zero-day » ciblant des infrastructures critiques, des logiciels largement utilisés et même des dispositifs IoT, illustrant une accélération alarmante de la découverte et de l'exploitation des vulnérabilités, souvent facilitée par l'IA.

**Points clés :**
*   **Automatisation des attaques :** Des chercheurs ont démontré qu'une IA peut identifier des vulnérabilités 70 fois plus vite qu'une analyse humaine, réduisant drastiquement les coûts pour les attaquants. L'émergence des « agents d'IA » permet désormais aux attaquants de déléguer l'exécution de ransomwares à des systèmes autonomes.
*   **Chaîne d'approvisionnement compromise :** Le package JavaScript `@ethersphere/bee-js` a été piégé pour voler des clés de portefeuilles et installer des backdoors sur Windows, Linux et macOS.
*   **IoT sous haute tension :** Des contrôleurs de réfrigération industrielle (Danfoss AK-SM 800A) sont vulnérables à des exécutions de code à distance (RCE) permettant le « brickage » définitif des appareils. De même, des caméras GeoVision sont exploitées pour miner de la cryptomonnaie via des pilotes vulnérables (BYOVD).
*   **Changement de politique Google :** Le Projet Zéro de Google durcit sa politique de divulgation : les vulnérabilités seront rendues publiques 90 jours après leur signalement, même sans correctif, avec une réduction prévue à 30 jours d'ici 2028.

**Vulnérabilités majeures :**
*   **CVE-2026-125350 :** Vulnérabilité *Use-After-Free* critique dans Google Chrome, déjà exploitée activement.
*   **SignDrop (Windows) :** Nouvelle faille d'escalade de privilèges via le système de fichiers *Common Log FileSystem (CLFS)*, détournant une fonctionnalité de sécurité en vecteur d'attaque pour obtenir les droits SYSTEM.
*   **Série CVE (XWEB EVO) :** Plusieurs failles critiques (dont **CVE-2026-124010**) permettent l'exécution de commandes root sur les contrôleurs de réfrigération, pour lesquelles aucun correctif ne sera déployé (fin de support).

**Recommandations :**
1.  **Mise à jour immédiate :** Appliquez les correctifs pour Chrome (v.157.0.8103.50+) et surveillez les avis de sécurité pour N-able N-central.
2.  **Audit des accès :** Supprimez systématiquement les mots de passe par défaut sur toutes les consoles d'administration exposées (ex: cas des constructeurs automobiles).
3.  **Renforcement des déploiements :** Ne vous reposez pas uniquement sur le « SHA pinning » pour vos workflows CI/CD ; les pipelines restent une cible de choix.
4.  **Gestion des actifs :** Identifiez et remplacez les équipements IoT ou serveurs ayant atteint leur fin de vie (End-of-Support), comme certains contrôleurs industriels, qui ne recevront plus aucun patch de sécurité.

---
[Source](https://thehackernews.com/2026/11/weekly-recap-n-able-0-days-windows-0.html){:target="_blank"}
