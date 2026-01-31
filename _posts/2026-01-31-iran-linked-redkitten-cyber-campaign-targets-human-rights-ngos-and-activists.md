---
title: 'Iran-Linked RedKitten Cyber Campaign Targets Human Rights NGOs and Activists'
date: 2026-01-31
permalink: /posts/2026/01/31/iran-linked-redkitten-cyber-campaign-targets-human-rights-ngos-and-activists/
tags:
- veille-cyber
- hackernews
---
## Campagne RedKitten : Une Cyberguerre Iranienne Ciblée

Une campagne cybernétique, baptisée RedKitten, orchestrée par un acteur de menace affilié à l'Iran, vise des ONG et des militants des droits de l'homme. Cette offensive survient dans un contexte de troubles civils en Iran, marqués par des manifestations contre l'inflation et une répression sévère.

**Points Clés :**

*   **Tactiques d'Ingénierie Sociale Sophistiquées :** La campagne utilise des documents Excel infectés, se faisant passer pour des rapports sur les victimes des manifestations, afin de tromper les cibles.
*   **Exploitation de l'IA :** L'utilisation potentielle de grands modèles linguistiques (LLM) pour construire et orchestrer les outils malveillants est une caractéristique notable, rendant la détection plus complexe.
*   **Infrastructure Cloud :** L'attaquant s'appuie sur des services cloud tels que GitHub et Google Drive pour la configuration et la récupération de modules, ainsi que sur Telegram pour le commandement et le contrôle (C2).
*   **Rétro-ingénierie et Persistance :** Le malware, nommé SloppyMIO, est capable d'exécuter des commandes, de collecter et d'exfiltrer des fichiers, et d'établir une persistance via des tâches planifiées.

**Vulnérabilités Exploités :**

L'article ne mentionne pas de CVE spécifiques pour les vulnérabilités exploitées. Cependant, les méthodes incluent :

*   **Exécution de Macros VBA malveillantes :** Les documents Excel contiennent des macros VBA qui, une fois activées par l'utilisateur, déclenchent le téléchargement et l'exécution du code malveillant.
*   **AppDomainManager Injection :** Une technique utilisée pour injecter un implant C# ("AppVStreamingUX_Multi_User.dll") dans des processus légitimes.

**Recommandations :**

Bien que l'article ne fournisse pas de liste exhaustive de recommandations, on peut déduire les points suivants pour la protection :

*   **Vigilance Accrue :** Faire preuve d'une extrême prudence face aux documents joints provenant de sources non fiables, en particulier ceux contenant des macros.
*   **Désactivation des Macros :** Désactiver l'exécution automatique des macros dans les applications de bureautique.
*   **Authentification Forte :** Utiliser l'authentification à deux facteurs (2FA) pour tous les comptes en ligne critiques, tels que Gmail et WhatsApp.
*   **Surveillance Réseau :** Mettre en place une surveillance réseau pour détecter les communications suspectes avec des services cloud ou des plateformes de messagerie.
*   **Connaissance des Menaces :** Se tenir informé des campagnes de phishing et des techniques d'attaquants émergentes, notamment celles exploitant l'IA.

---
[Source](https://thehackernews.com/2026/01/iran-linked-redkitten-cyber-campaign.html){:target="_blank"}
