---
title: 'Brazilian LofyGang Resurfaces After Three Years With Minecraft LofyStealer Campaign'
date: 2026-04-28
permalink: /posts/2026/04/28/brazilian-lofygang-resurfaces-after-three-years-with-minecraft-lofystealer-campaign/
tags:
- veille-cyber
- hackernews
---
### Retour du groupe LofyGang : La campagne "LofyStealer" cible les joueurs de Minecraft

Le groupe cybercriminel brésilien LofyGang est de retour après trois ans d'inactivité avec une nouvelle campagne malveillante. Cette fois, ils ciblent les joueurs de Minecraft via un logiciel de triche (« cheat ») contrefait nommé « Slinky », conçu pour déployer le malware **LofyStealer** (alias GrabBot).

**Points clés :**
* **Mode opératoire :** Le malware se présente sous la forme d'un outil de triche légitime pour Minecraft. Une fois exécuté, un chargeur JavaScript déploie le stealer en mémoire pour éviter la détection.
* **Objectifs :** Exfiltration massive de données sensibles (cookies, mots de passe, jetons de session, coordonnées bancaires et IBAN) provenant de nombreux navigateurs web (Chrome, Edge, Firefox, Brave, Opera, etc.).
* **Évolution :** Le groupe a adopté un modèle de « Malware-as-a-Service » (MaaS) avec des versions gratuites et payantes, incluant un constructeur de malwares baptisé « Slinky Cracked ».
* **Contexte élargi :** Cette attaque s'inscrit dans une tendance croissante où des plateformes de confiance (GitHub, Reddit) sont détournées via l'empoisonnement SEO pour distribuer des logiciels malveillants sous couvert d'outils de jeu, de scripts ou de logiciels de sécurité.

**Vulnérabilités :**
* Il n'existe pas de CVE spécifique exploitée, car l'attaque repose sur l'ingénierie sociale et la confiance des utilisateurs dans les plateformes de téléchargement open-source.
* **Vecteurs :** Abus de la chaîne d'approvisionnement logicielle, typosquattage, et détournement de l'image de marque de plateformes comme GitHub pour héberger des dépôts frauduleux.

**Recommandations :**
* **Méfiance envers les outils tiers :** Ne jamais télécharger ou exécuter de logiciels de « triche » ou de modifications non officielles, car ils constituent des vecteurs d'infection privilégiés.
* **Vigilance sur les dépôts :** Traiter avec suspicion tout téléchargement provenant de GitHub qui combine un interpréteur renommé avec des fichiers de données opaques.
* **Sécurité des comptes :** Utiliser l'authentification multifacteur (MFA) sur tous les comptes critiques (Discord, services bancaires, réseaux sociaux) pour limiter l'impact en cas de vol de jetons.
* **Surveillance :** Prioriser l'analyse des processus suspects tentant d'accéder aux répertoires de données des navigateurs (fichiers de cookies et de mots de passe).

---
[Source](https://thehackernews.com/2026/04/brazilian-lofygang-resurfaces-after.html){:target="_blank"}
