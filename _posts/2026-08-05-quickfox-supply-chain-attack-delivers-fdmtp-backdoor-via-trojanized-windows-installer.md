---
title: 'QuickFox Supply Chain Attack Delivers FDMTP Backdoor via Trojanized Windows Installer'
date: 2026-08-05
permalink: /posts/2026/08/05/quickfox-supply-chain-attack-delivers-fdmtp-backdoor-via-trojanized-windows-installer/
tags:
- veille-cyber
- hackernews
---
### Attaque de chaîne d'approvisionnement via le VPN QuickFox

Une campagne d'attaque par chaîne d'approvisionnement a compromis le logiciel VPN QuickFox, ciblant principalement les utilisateurs de Windows. Des attaquants, possiblement liés au groupe Mustang Panda, ont injecté un code malveillant dans l'installateur officiel du logiciel afin de déployer la porte dérobée FDMTP.

**Points clés :**
*   **Vecteur :** Une version corrompue de l'installateur Windows de QuickFox (versions 3.0.51.0 à 3.59.5).
*   **Mécanisme :** Utilisation de scripts JavaScript injectés dans un fichier HTML pour télécharger des charges utiles depuis un domaine frauduleux (`cdns3.51quickfox[.]cn`) imitant l'original.
*   **Ciblage sélectif :** Le logiciel effectue une reconnaissance de la machine victime. Il interrompt l'installation si certains processus sont détectés (Steam) ou si des outils spécifiques (développement, crypto-monnaies, outils de gestion à distance) sont absents, afin d'éviter les environnements non désirés.
*   **Persistance :** Utilisation de la technique de *DLL side-loading* pour charger la porte dérobée FDMTP.
*   **Objectifs :** Exfiltration d'informations système, espionnage des processus en cours, et exécution de plugins distants.

**Vulnérabilités :**
*   Aucune CVE spécifique n'est associée, car il s'agit d'une compromission directe du processus de distribution du logiciel par des attaquants.

**Recommandations :**
*   **Mise à jour immédiate :** Les utilisateurs doivent impérativement mettre à jour QuickFox vers la version **3.59.6** ou supérieure, qui a été nettoyée des composants malveillants.
*   **Vigilance logicielle :** Privilégier le téléchargement des applications uniquement depuis les sites officiels et vérifier, si possible, les sommes de contrôle (hashes) des exécutables.
*   **Analyse comportementale :** Surveiller les accès réseau suspects et la présence de processus inconnus tentant de charger des DLL dans des dossiers d'applications légitimes.

---
[Source](https://thehackernews.com/2026/08/quickfox-supply-chain-attack-delivers.html){:target="_blank"}
