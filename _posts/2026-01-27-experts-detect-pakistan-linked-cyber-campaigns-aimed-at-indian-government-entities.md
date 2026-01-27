---
title: 'Experts Detect Pakistan-Linked Cyber Campaigns Aimed at Indian Government Entities'
date: 2026-01-27
permalink: /posts/2026/01/27/experts-detect-pakistan-linked-cyber-campaigns-aimed-at-indian-government-entities/
tags:
- veille-cyber
- hackernews
---
**Campagnes de cyberattaques ciblées sur des entités gouvernementales indiennes**

Des campagnes de cyberattaques, attribuées à un groupe d'acteurs malveillants basé au Pakistan, ont ciblé des entités gouvernementales indiennes. Ces campagnes, baptisées "Gopher Strike" et "Sheet Attack", utilisent des techniques inédites et montrent des similitudes avec le groupe APT36, bien qu'elles puissent provenir d'un nouveau sous-groupe ou d'un groupe indépendant.

**Points Clés :**

*   **Ciblage géographique :** Des entités gouvernementales indiennes sont visées.
*   **Origine présumée :** Un acteur lié au Pakistan, potentiellement un nouveau sous-groupe de l'APT36 ou un groupe parallèle.
*   **Méthodologie :** Utilisation d'emails de phishing, de documents PDF trompeurs, et de services légitimes (Google Sheets, Firebase, email) pour le commandement et le contrôle (C2).
*   **Techniques d'évasion :** Les attaques incluent des vérifications côté serveur pour éviter l'analyse automatique des fichiers malveillants et l'augmentation artificielle de la taille des exécutables pour contourner les antivirus.

**Vulnérabilités et Outils Utilisés :**

*   **Gopher Strike :** Utilise des emails de phishing délivrant des PDF contenant une image floutée et une fausse fenêtre de mise à jour Adobe Acrobat Reader DC. Le téléchargement du fichier ISO malveillant n'est déclenché que si la requête provient d'une adresse IP indienne et correspond à un agent utilisateur Windows.
    *   **Outil de téléchargement :** GOGITTER (basé sur Golang) est utilisé pour créer un script VBScript, établir la persistance via une tâche planifiée, et télécharger un fichier "adobe_update.zip" depuis un dépôt GitHub privé.
*   **Sheet Attack :** Tire son nom de l'utilisation de services légitimes comme Google Sheets, Firebase et l'email pour le C2.
*   **GITSHELLPAD :** Un backdoor léger basé sur Golang, utilisant des dépôts GitHub privés pour le C2, en interrogeant le fichier "command.txt" pour obtenir des instructions.
    *   **Commandes supportées par GITSHELLPAD :** `cd ..`, `cd`, `run`, `upload`, `download`, et une commande par défaut utilisant `cmd /c`. Les résultats sont stockés dans "result.txt" et uploadés sur GitHub.
*   **GOSHELL :** Un chargeur Golang personnalisé utilisé pour délivrer Cobalt Strike Beacon après plusieurs étapes de décodage. Sa taille est gonflée artificiellement pour éviter la détection antivirus et il s'exécute uniquement sur des noms d'hôtes spécifiques.

Il n'y a pas de CVE spécifiquement mentionnés dans l'article pour ces campagnes, mais les techniques visent à exploiter la confiance des utilisateurs et à contourner les mesures de sécurité existantes.

**Recommandations :**

Bien que l'article ne détaille pas explicitement de recommandations de sécurité, les méthodes d'attaque suggèrent les points suivants pour une meilleure défense :

*   **Sensibilisation et formation à la cybersécurité :** Former les utilisateurs à identifier les emails de phishing et les documents suspects.
*   **Surveillance des communications :** Analyser le trafic réseau et les connexions vers des services cloud et des dépôts de code suspects.
*   **Détection avancée des menaces :** Utiliser des solutions capables de détecter des comportements malveillants inhabituels, y compris l'exécution de scripts et l'utilisation de services légitimes à des fins malveillantes.
*   **Gestion des vulnérabilités et mises à jour :** S'assurer que tous les logiciels, y compris Adobe Acrobat Reader, sont à jour pour atténuer les vulnérabilités connues.
*   **Authentification forte :** Mettre en place des mesures d'authentification robustes pour protéger l'accès aux systèmes et aux dépôts de code.
*   **Journalisation et analyse :** Maintenir des journaux d'activité détaillés et les analyser régulièrement pour détecter toute activité suspecte.

---
[Source](https://thehackernews.com/2026/01/experts-detect-pakistan-linked-cyber.html){:target="_blank"}
