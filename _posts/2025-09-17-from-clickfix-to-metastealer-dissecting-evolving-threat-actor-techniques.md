---
title: 'From ClickFix to MetaStealer: Dissecting Evolving Threat Actor Techniques'
date: 2025-09-17
permalink: /posts/2025/09/17/from-clickfix-to-metastealer-dissecting-evolving-threat-actor-techniques/
tags:
- veille-cyber
- bleepingcomp
---
**Évolution des Techniques des Acteurs de Menaces : Du ClickFix au MetaStealer**

Une analyse récente met en évidence l'intensification des activités malveillantes, combinant des tactiques d'ingénierie sociale éprouvées avec des chaînes d'infection sophistiquées. Des attaques simulant une vérification Cloudflare pour déguiser un installateur AnyDesk malveillant ont été observées. Ce dernier, loin de suivre le modèle classique du ClickFix, utilise l'Explorateur de fichiers Windows et un package MSI masqué en PDF pour déployer le malware MetaStealer. Parallèlement, des incidents impliquant la variante de ransomware Cephalus ont été détectés, utilisant le DLL sideloading via une application SentinelOne légitime pour lancer la charge utile.

**Points Clés :**

*   **Évolution du ClickFix :** Les attaques de type ClickFix, qui exploitent les CAPTCHAs pour inciter les utilisateurs à exécuter des commandes, évoluent. Des variantes comme "FileFix" détournent vers l'Explorateur de fichiers au lieu de la boîte de dialogue "Exécuter".
*   **Nouvelle Chaîne d'Infection :** Une nouvelle méthode combine une fausse page de vérification Cloudflare (turnstile) avec l'Explorateur de fichiers Windows via le protocole `search-ms`.
*   **Utilisation de Fichiers Masqués :** Un fichier raccourci LNK, déguisé en PDF (Readme Anydesk.pdf), est utilisé pour télécharger et exécuter un package MSI.
*   **Vol d'Informations Sensibles :** Le package MSI installe MetaStealer, un voleur d'informations capable de récupérer des identifiants et des fichiers, et d'exploiter des portefeuilles de cryptomonnaies. Il est également capable de récupérer le nom de l'ordinateur de la victime comme sous-domaine.
*   **Ransomware Cephalus :** Cette variante utilise le DLL sideloading avec l'exécutable légitime `SentinelBrowserNativeHost.exe` de SentinelOne.

**Vulnérabilités et Vecteurs d'Attaque :**

*   **Ingénierie Sociale :** Exploitation de la confiance des utilisateurs via de fausses pages de vérification (Cloudflare Turnstile) et des leurres (faux installateurs AnyDesk, faux PDF).
*   **DLL Sideloading :** Utilisation de librairies dynamiques légitimes pour exécuter du code malveillant (Cephalus).
*   **Exploitation de Fonctionnalités Légitimes :** Utilisation du protocole `search-ms` de Windows pour orienter vers des partages réseau contrôlés par l'attaquant.
*   **Masquage de Fichiers :** Utilisation d'extensions de fichiers trompeuses (LNK comme PDF).
*   **Pas de CVE spécifique mentionné dans l'article.**

**Recommandations :**

*   **Éducation des Utilisateurs :** Former les utilisateurs à reconnaître les leurres liés aux attaques de type ClickFix, notamment les CAPTCHAs demandant de copier-coller des commandes ou de naviguer vers l'Explorateur de fichiers.
*   **Restrictions d'Utilisation :** Si pertinent, limiter l'utilisation de la boîte de dialogue "Exécuter" de Windows pour les tâches quotidiennes.
*   **Surveillance du Trafic Réseau :** Surveiller les communications avec des domaines et adresses IP suspects, particulièrement ceux associés à des téléchargements ou à des communications de type C2.
*   **Analyse des Fichiers Suspects :** Examiner les fichiers téléchargés, en particulier ceux provenant de sources non fiables ou déguisés.
*   **Maintien de la Vigilance :** Rester informé des nouvelles techniques d'attaque et des tendances en matière de logiciels malveillants.

---
[Source](https://www.bleepingcomputer.com/news/security/from-clickfix-to-metastealer-dissecting-evolving-threat-actor-techniques/){:target="_blank"}
