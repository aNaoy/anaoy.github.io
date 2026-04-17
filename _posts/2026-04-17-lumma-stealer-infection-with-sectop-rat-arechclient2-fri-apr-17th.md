---
title: 'Lumma Stealer infection with Sectop RAT (ArechClient2), (Fri, Apr 17th)'
date: 2026-04-17
permalink: /posts/2026/04/17/lumma-stealer-infection-with-sectop-rat-arechclient2-fri-apr-17th/
tags:
- veille-cyber
- sans-isc
---
### Analyse d'une campagne d'infection combinée : Lumma Stealer et Sectop RAT

Cette campagne d'infection illustre une méthode de distribution classique où des logiciels piratés servent de vecteur pour propager des malwares. Dans ce scénario, le téléchargement d'une application sous forme d'archive 7-zip protégée par mot de passe initie une infection en deux étapes : le déploiement du voleur d'informations **Lumma Stealer**, suivi de l'installation du **Sectop RAT** (ArechClient2) pour un contrôle persistant.

**Points clés :**
*   **Vecteur d'attaque :** Sites Web proposant des logiciels protégés par droits d'auteur en version "crackée".
*   **Technique d'évasion :** Utilisation d'archives protégées par mot de passe et d'exécutables "gonflés" (806 Mo) par ajout d'octets nuls pour contourner la détection antivirus et les analyses de taille.
*   **Chaîne d'infection :** L'exécutable initial (`appFile.exe`) déploie Lumma Stealer, qui télécharge ensuite une bibliothèque DLL malveillante (`NetGui.dll`) via `rundll32` pour activer le Sectop RAT.
*   **Persistance :** Le Sectop RAT assure sa présence sur le système infecté via des connexions C2 (Command & Control) spécifiques.

**Vulnérabilités :**
*   Aucune CVE spécifique n'est exploitée ici ; l'attaque repose sur l'ingénierie sociale et la compromission volontaire par l'utilisateur en téléchargeant des fichiers exécutables douteux.

**Recommandations :**
*   **Sensibilisation :** Éviter impérativement le téléchargement de logiciels piratés, de cracks ou de générateurs de clés, qui sont des vecteurs de distribution privilégiés pour les malwares.
*   **Filtrage réseau :** Bloquer les connexions vers les domaines C2 identifiés (ex: `cankgmr.cyou`, `strikql.shop`, `enotsosun.pw`) et surveiller les communications sortantes non chiffrées vers des adresses IP suspectes.
*   **Sécurité des points de terminaison :** Mettre en œuvre des politiques interdisant l'exécution de binaires non signés ou provenant de sources inconnues, et surveiller les processus suspects utilisant `rundll32.exe` depuis des répertoires temporaires (`AppData\Local\Temp`).
*   **Analyse de fichiers :** Utiliser des outils de sandbox pour inspecter tout fichier exécutable volumineux ou protégé par mot de passe avant exécution, en portant une attention particulière aux fichiers présentant des tailles anormales (remplissage d'octets nuls).

---
[Source](https://isc.sans.edu/diary/rss/32904){:target="_blank"}
