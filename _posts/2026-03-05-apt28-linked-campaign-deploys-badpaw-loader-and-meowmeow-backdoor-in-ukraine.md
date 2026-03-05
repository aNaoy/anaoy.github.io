---
title: 'APT28-Linked Campaign Deploys BadPaw Loader and MeowMeow Backdoor in Ukraine'
date: 2026-03-05
permalink: /posts/2026/03/05/apt28-linked-campaign-deploys-badpaw-loader-and-meowmeow-backdoor-in-ukraine/
tags:
- veille-cyber
- hackernews
---
### Campagne d'espionnage APT28 : Les malwares BadPaw et MeowMeow frappent l'Ukraine

Une nouvelle campagne cybercriminelle, attribuée au groupe russe APT28, cible des entités ukrainiennes via des techniques sophistiquées d'ingénierie sociale et des malwares inédits.

**Points clés :**
*   **Vecteur d'attaque :** Hameçonnage par e-mail (via ukr.net) contenant un lien vers une archive ZIP.
*   **Ingénierie sociale :** Utilisation d'un faux document relatif aux demandes de passage aux frontières pour masquer l'exécution du malware.
*   **Chaîne d'infection :** L'archive déploie un fichier HTA qui exécute un script VBS, lequel extrait le chargeur (loader) **BadPaw** caché dans une image PNG. Ce dernier télécharge ensuite la porte dérobée (backdoor) **MeowMeow**.
*   **Mécanismes d'évasion :** Les malwares vérifient l'ancienneté du système (âge de l'OS) et détectent la présence d'outils d'analyse (Wireshark, Procmon, etc.) ou de bacs à sable (sandbox) avant de s'exécuter.
*   **Capacités de MeowMeow :** Exécution de commandes PowerShell à distance et gestion complète du système de fichiers.

**Vulnérabilités exploitées :**
*   Bien que l'article mentionne une implication historique d'APT28 avec la vulnérabilité **CVE-2026-21513** (MSHTML), cette campagne repose principalement sur l'exécution malveillante de fichiers HTA et de scripts VBS par l'utilisateur.

**Recommandations :**
*   **Sensibilisation :** Former les utilisateurs à la méfiance envers les e-mails non sollicités, particulièrement ceux incitant à télécharger des archives ZIP.
*   **Sécurité des terminaux :** Bloquer l'exécution automatique des fichiers HTA et des scripts (VBScript/PowerShell) via des politiques de restriction logicielle (AppLocker ou WDAC).
*   **Monitoring :** Surveiller les processus suspects créant des tâches planifiées ou tentant d'exécuter du code dissimulé dans des fichiers images.
*   **Protection :** S'assurer que les solutions EDR/antivirus sont configurées pour détecter les comportements d'évasion typiques des malwares (détection de sandbox, requêtes système anormales).

---
[Source](https://thehackernews.com/2026/03/apt28-linked-campaign-deploys-badpaw.html){:target="_blank"}
