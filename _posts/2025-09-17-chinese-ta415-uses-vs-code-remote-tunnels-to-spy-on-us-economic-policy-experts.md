---
title: 'Chinese TA415 Uses VS Code Remote Tunnels to Spy on U.S. Economic Policy Experts'
date: 2025-09-17
permalink: /posts/2025/09/17/chinese-ta415-uses-vs-code-remote-tunnels-to-spy-on-us-economic-policy-experts/
tags:
- veille-cyber
- hackernews
---
## Espionnage Économique : TA415 Exploite VS Code pour Cibler les Experts Américains

Un acteur de menace aligné sur la Chine, connu sous le nom de TA415, mène des campagnes de hameçonnage ciblées contre le gouvernement américain, des groupes de réflexion et des organisations universitaires. Ces attaques utilisent des prétextes liés à l'économie sino-américaine pour inciter les victimes à télécharger des fichiers malveillants.

Observée durant les mois de juillet et août 2025, cette activité vise à recueillir des renseignements dans le contexte des pourparlers commerciaux actuels entre les États-Unis et la Chine. Ce groupe présente des similitudes avec les clusters de menace APT41 et Brass Typhoon.

Les messages de hameçonnage, usurpant l'identité du U.S.-China Business Council, invitent les destinataires à des séances d'information confidentielles sur les affaires sino-américaines et sino-taïwanaises. Ils sont envoyés depuis une adresse zoho mail et utilisent le service Cloudflare WARP pour masquer leur origine. Ces e-mails contiennent des liens vers des archives protégées par mot de passe hébergées sur des services de partage cloud (Zoho WorkDrive, Dropbox, OpenDrive).

Ces archives incluent un raccourci Windows (fichier LNK) qui exécute un script batch. Ce script affiche un document PDF en guise de diversion tout en lançant en arrière-plan un chargeur Python obscurci nommé WhirlCoil. Ce chargeur, récupéré précédemment depuis des sites comme Pastebin, a la capacité d'établir une persistance en créant une tâche planifiée (par exemple, GoogleUpdate ou MicrosoftHealthcareMonitorNode) s'exécutant toutes les deux heures avec des privilèges SYSTEM si disponibles.

Le chargeur Python établit ensuite un tunnel distant Visual Studio Code pour obtenir un accès backdoor persistant. Il récolte des informations sur le système et le contenu de divers répertoires utilisateur. Ces données, ainsi que le code de vérification du tunnel distant, sont envoyés à un service de journalisation de requêtes (comme requestrepo[.]com) sous forme de données encodées en base64 dans des requêtes HTTP POST. L'acteur de menace utilise ensuite ces informations pour s'authentifier auprès du tunnel VS Code, accéder au système de fichiers et exécuter des commandes arbitraires via le terminal intégré de Visual Studio. La chaîne d'infection observée est similaire à celle utilisée dans une attaque antérieure en septembre 2024 ciblant les secteurs de l'aérospatiale, de la chimie, de l'assurance et de la fabrication.

### Points Clés :

*   **Acteur de Menace :** TA415 (aligné sur la Chine), également lié à APT41 et Brass Typhoon.
*   **Objectif :** Cyberespionnage, collecte de renseignements sur la politique économique et les relations sino-américaines.
*   **Méthode d'Entrée :** Campagnes de hameçonnage ciblées.
*   **Outils :**
    *   Faux e-mails d'invitation (usurpation d'identité du U.S.-China Business Council).
    *   Services de partage cloud pour héberger les charges utiles.
    *   Fichiers LNK et scripts batch pour l'exécution initiale.
    *   Chargeur Python obscurci (WhirlCoil).
    *   Tâches planifiées pour la persistance.
    *   Tunnels distants Visual Studio Code (VS Code Remote Tunnels) pour l'accès backdoor.
    *   Services de journalisation de requêtes pour l'exfiltration de données.
*   **Cibles :** Experts américains en politique économique, organisations gouvernementales, groupes de réflexion et institutions académiques.
*   **Contexte :** Pourparlers commerciaux États-Unis-Chine.

### Vulnérabilités :

*   **Aucune vulnérabilité logicielle spécifique (CVE) n'est explicitement mentionnée dans l'article.** L'exploitation repose sur l'ingénierie sociale (hameçonnage) et l'utilisation d'outils légitimes (VS Code Remote Tunnels) détournés à des fins malveillantes. La capacité d'un utilisateur à exécuter des fichiers ou à configurer des tunnels VS Code est exploitée.

### Recommandations :

*   **Vigilance face au hameçonnage :** Les utilisateurs doivent être extrêmement prudents avec les e-mails inattendus, surtout s'ils contiennent des liens ou des pièces jointes, et vérifier l'authenticité de l'expéditeur.
*   **Sensibilisation à la sécurité :** Renforcer la formation des employés sur les menaces de cybersécurité, y compris le hameçonnage et l'ingénierie sociale.
*   **Surveillance du réseau et des points d'accès :** Mettre en place une surveillance adéquate pour détecter les connexions suspectes ou inhabituelles, notamment celles impliquant des tunnels distants ou des communications vers des services de journalisation de requêtes inconnus.
*   **Contrôle strict des privilèges :** Appliquer le principe du moindre privilège pour limiter les actions qu'un processus malveillant pourrait effectuer, même s'il est exécuté avec des privilèges élevés.
*   **Restrictions sur l'utilisation de certains outils :** Les organisations pourraient envisager des politiques concernant l'installation et l'utilisation d'outils de développement comme Visual Studio Code, en particulier leurs fonctionnalités de tunneling, et mettre en place des mesures de contrôle pour prévenir leur utilisation malveillante.

---
[Source](https://thehackernews.com/2025/09/chinese-ta415-uses-vs-code-remote.html){:target="_blank"}
