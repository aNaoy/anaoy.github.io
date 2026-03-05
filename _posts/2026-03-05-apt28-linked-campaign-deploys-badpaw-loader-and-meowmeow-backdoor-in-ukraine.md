---
title: 'APT28-Linked Campaign Deploys BadPaw Loader and MeowMeow Backdoor in Ukraine'
date: 2026-03-05
permalink: /posts/2026/03/05/apt28-linked-campaign-deploys-badpaw-loader-and-meowmeow-backdoor-in-ukraine/
tags:
- veille-cyber
- hackernews
---
## Campagne Russe en Ukraine : Déploiement de BadPaw et MeowMeow

Une nouvelle campagne cybernétique d'origine russe a ciblé des entités ukrainiennes en utilisant deux familles de malwares inédites : BadPaw et MeowMeow. L'attaque débute par un email de phishing contenant un lien vers une archive ZIP. Une fois décompressée, celle-ci exécute un fichier HTA affichant un document leurre en ukrainien, simulant un appel concernant le passage de frontières pour tromper la victime.

Simultanément, une charge utile .NET nommée BadPaw est déployée. Ce loader établit une connexion avec un serveur distant pour télécharger et installer une backdoor sophistiquée, MeowMeow. Cette campagne est attribuée avec une confiance modérée au groupe APT28, lié à l'État russe, en raison du ciblage, de la nature géopolitique des leurres et des recoupements avec des opérations cybernétiques russes antérieures.

L'email de phishing provient de ukr[.]net, dans le but d'établir une crédibilité. Le lien redirige vers une image de très petite taille, agissant comme un pixel de suivi pour confirmer le clic. Une seconde redirection mène au téléchargement de l'archive ZIP.

Le fichier HTA, une fois lancé, dépose un document leurre pour distraire l'utilisateur tout en exécutant discrètement les étapes suivantes. Pour éviter la détection par des environnements de sandbox, le malware vérifie l'ancienneté du système d'exploitation. Si le système est jugé légitime, le HTA extrait un script VBScript et une image PNG. Un scheduled task est créé pour garantir la persistance du VBScript.

Le VBScript a pour rôle d'extraire du code malveillant caché dans l'image PNG. Ce code, appelé BadPaw, est un loader obfusqué capable de communiquer avec un serveur de commande et contrôle (C2) pour télécharger d'autres composants, dont un exécutable nommé MeowMeow.

BadPaw intègre un mécanisme de leurre : s'il est exécuté indépendamment de la chaîne d'attaque complète, il affiche une interface graphique (GUI) avec une image de chat et un message "Meow Meow Meow", afin de tromper une analyse manuelle.

La backdoor MeowMeow n'est activée que lorsqu'elle est exécutée avec un paramètre spécifique ("-v") fourni par la chaîne d'infection initiale, après avoir vérifié l'absence d'outils d'analyse forensique (comme Wireshark, Procmon, Ollydbg, Fiddler). MeowMeow est capable d'exécuter à distance des commandes PowerShell et de manipuler le système de fichiers (lecture, écriture, suppression de données). La présence de chaînes de caractères en russe dans le code source renforce l'hypothèse d'un acteur russophone.

**Points Clés :**

*   **Campagne d'APT28 ciblant l'Ukraine.**
*   **Utilisation de deux malwares inédits : BadPaw (loader) et MeowMeow (backdoor).**
*   **Méthode d'infection initiale par phishing avec archive ZIP et fichier HTA.**
*   **Utilisation de leurres pour tromper les victimes.**
*   **Mécanismes d'anti-analyse et de persistance.**
*   **Capacités de la backdoor : exécution de commandes à distance, manipulation de fichiers.**

**Vulnérabilités:**

*   Aucune vulnérabilité spécifique avec des identifiants CVE n'est mentionnée dans l'article pour les malwares eux-mêmes. L'attaque repose sur l'ingénierie sociale et l'exploitation de la confiance des utilisateurs.

**Recommandations:**

*   **Vigilance accrue face aux emails de phishing.**
*   **Prudence lors de l'ouverture de pièces jointes et du téléchargement d'archives provenant de sources inconnues ou suspectes.**
*   **Maintien des systèmes d'exploitation et des logiciels de sécurité à jour.**
*   **Sensibilisation des utilisateurs aux techniques d'ingénierie sociale utilisées par les acteurs malveillants.**
*   **Mise en place de mesures de sécurité réseau robustes pour détecter et bloquer les communications C2.**

---
[Source](https://thehackernews.com/2026/03/apt28-linked-campaign-deploys-badpaw.html){:target="_blank"}
