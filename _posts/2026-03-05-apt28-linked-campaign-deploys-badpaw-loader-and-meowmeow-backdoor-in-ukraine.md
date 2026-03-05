---
title: 'APT28-Linked Campaign Deploys BadPaw Loader and MeowMeow Backdoor in Ukraine'
date: 2026-03-05
permalink: /posts/2026/03/05/apt28-linked-campaign-deploys-badpaw-loader-and-meowmeow-backdoor-in-ukraine/
tags:
- veille-cyber
- hackernews
---
### Campagne Russe Ciblée sur l'Ukraine : Déploiement de BadPaw et MeowMeow

Une campagne de cybercriminalité d'origine russe a visé des entités ukrainiennes en utilisant deux nouvelles familles de logiciels malveillants : BadPaw et MeowMeow. Les recherches indiquent une attribution de forte probabilité à APT28, un groupe parrainé par l'État russe, en raison de la nature des cibles, des leurres géopolitiques et des recoupements avec des opérations antérieures.

L'attaque débute par un courriel de phishing contenant un lien vers une archive ZIP. Après extraction, un fichier HTA affiche un document trompeur en ukrainien sur des appels de franchissement de frontière pour tromper la victime. En parallèle, un chargeur basé sur .NET, nommé BadPaw, est déployé. Ce dernier établit une communication avec un serveur distant pour télécharger et installer une porte dérobée sophistiquée, MeowMeow.

BadPaw, s'il est exécuté indépendamment, affiche une interface graphique avec une image de chat, un leurre visuel associé au fichier initial. L'activation de MeowMeow se fait via un paramètre spécifique et après vérification qu'il ne s'exécute pas dans un environnement de simulation ou avec des outils d'analyse activement présents. MeowMeow permet l'exécution à distance de commandes PowerShell et la manipulation de fichiers sur le système compromis. La présence de chaînes de caractères en russe dans le code renforce l'hypothèse d'une origine russe, potentiellement une erreur de sécurité opérationnelle ou un vestige du développement.

**Points Clés :**

*   **Cible Principale :** Entités ukrainiennes.
*   **Auteur Présumé :** APT28 (parrainé par la Russie).
*   **Méthode d'Entrée :** Phishing par courriel avec une archive ZIP.
*   **Leurres :** Document trompeur en ukrainien sur le franchissement de frontière, interface graphique avec un chat pour les analyses manuelles.
*   **Logiciels Malveillants :** BadPaw (chargeur .NET) et MeowMeow (porte dérobée).
*   **Techniques :** Utilisation d'archives ZIP, fichiers HTA, VBScript, obfuscation dans des images PNG, scheduled tasks pour la persistance, vérifications anti-sandbox et anti-analyse.

**Vulnérabilités Exploités :**

Aucune vulnérabilité logicielle spécifique (CVE) n'est explicitement mentionnée dans l'article pour l'infection initiale. L'attaque repose principalement sur l'ingénierie sociale et l'exécution de code malveillant par l'utilisateur. Cependant, la capacité de MeowMeow à exécuter des commandes à distance et à manipuler des fichiers exploite les privilèges du compte utilisateur compromis sur le système.

**Recommandations :**

*   **Sensibilisation aux Phishing :** Former les utilisateurs à reconnaître et signaler les courriels de phishing suspects, notamment ceux contenant des liens vers des archives ou des fichiers exécutables inattendus.
*   **Vérification des Liens et Fichiers :** Être prudent lors de la réception de fichiers ZIP ou de liens provenant de sources inconnues ou non vérifiées.
*   **Gestion des Permissions :** Appliquer le principe du moindre privilège pour limiter l'impact d'une compromission éventuelle.
*   **Sécurité des Points d'Extrémité :** Maintenir à jour les logiciels antivirus et les solutions de sécurité endpoint, et surveiller les activités suspectes.
*   **Analyse et Détection :** Mettre en place des mécanismes de détection des logiciels malveillants connus et des comportements suspects, tels que l'exécution de scripts inconnus ou la création de tâches planifiées inhabituelles.
*   **Segmentation Réseau :** Isoler les systèmes sensibles pour limiter la propagation latérale en cas de compromission.

---
[Source](https://thehackernews.com/2026/03/apt28-linked-campaign-deploys-badpaw.html){:target="_blank"}
