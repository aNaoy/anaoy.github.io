---
title: 'Microsoft releases Windows 11 OOB hotpatch to fix RRAS RCE flaw'
date: 2026-03-15
permalink: /posts/2026/03/15/microsoft-releases-windows-11-oob-hotpatch-to-fix-rras-rce-flaw/
tags:
- veille-cyber
- bleepingcomp
---
### Correctif d'urgence pour Windows 11 : Vulnérabilités RRAS

Microsoft a publié un correctif « hotpatch » hors cycle (KB5084597) destiné aux versions Entreprise de Windows 11 (25H2, 24H2 et LTSC 2024). Ce déploiement permet de sécuriser des systèmes critiques sans nécessiter de redémarrage immédiat, en appliquant les correctifs directement en mémoire.

**Points clés :**
* **Cible :** Systèmes Windows 11 Entreprise utilisant le programme « hotpatch » via Windows Autopatch.
* **Fonctionnement :** Le correctif applique les modifications en mémoire pour une protection immédiate tout en mettant à jour les fichiers sur le disque pour une persistance après redémarrage.
* **Contexte :** Ces vulnérabilités avaient été traitées lors du *Patch Tuesday* de mars 2026, mais ce déploiement complémentaire garantit une couverture étendue pour les environnements de gestion de serveurs distants.

**Vulnérabilités corrigées :**
* **CVE-2026-25172**
* **CVE-2026-25173**
* **CVE-2026-26111**
* *Description :* Ces failles concernent l'outil de gestion « Routing and Remote Access Service » (RRAS). Un attaquant authentifié peut exploiter ces vulnérabilités en incitant un utilisateur du domaine à envoyer une requête vers un serveur malveillant, menant à une exécution de code à distance (RCE).

**Recommandations :**
* Les administrateurs gérant des parcs via Windows Autopatch doivent s'assurer que la mise à jour KB5084597 est correctement distribuée sur les machines éligibles.
* Bien que le hotpatch évite un redémarrage immédiat, il est recommandé de planifier un redémarrage ultérieur pour finaliser l'application des correctifs sur le disque de manière conventionnelle.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-releases-windows-11-oob-hotpatch-to-fix-rras-rce-flaw/){:target="_blank"}
