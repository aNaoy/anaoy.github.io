---
title: 'GOLD SALEM tradecraft for deploying Warlock ransomware'
date: 2025-12-11
permalink: /posts/2025/12/11/gold-salem-tradecraft-for-deploying-warlock-ransomware/
tags:
- veille-cyber
- sophos
---
### Activité du groupe GOLD SALEM et déploiement du ransomware Warlock

Le groupe cybercriminel GOLD SALEM, actif depuis mars 2025, utilise une combinaison de techniques et d'outils pour déployer le ransomware Warlock. L'accès initial s'effectue fréquemment via l'exploitation de vulnérabilités dans les environnements SharePoint, y compris l'utilisation de la chaîne d'exploitation "ToolShell".

Le groupe exploite des outils légitimes tels que Velociraptor, normalement utilisé pour la réponse aux incidents, mais détourné ici pour des activités malveillantes. L'infrastructure de commande et de contrôle (C2) repose souvent sur des domaines hébergés sur Cloudflare Workers (sous le domaine `workers.dev`).

**Points Clés et Vulnérabilités :**

*   **Accès Initial :** Exploitation de vulnérabilités SharePoint (potentiellement zero-day, comme ToolShell).
*   **Outils:** Utilisation de Velociraptor, Visual Studio Code (VS Code) en mode tunnel, Cloudflared pour le tunneling, Mimikatz pour le vol d'identifiants, des scripts batch, et des outils pour l'inventaire système et le vidage de mots de passe Veeam.
*   **Persistance :** Création de comptes administrateur avec des mots de passe faibles (ex: `abcd1234`).
*   **Évasion de Défense :** Emploi d'un outil tueur d'antivirus (AV) et EDR (`vmtools.exe`) et utilisation de pilotes vulnérables (BYOVD) pour désactiver les solutions de sécurité. Des techniques de side-loading de DLL sont également observées.
*   **Infrastructure C2 :** Utilisation de domaines `workers.dev` pour héberger les outils et établir des tunnels.
*   **Ransomwares Utilisés :** Principalement Warlock (.x2anylock, .xlockxlock), mais aussi LockBit 3.0 et Babuk.
*   **Contact Ransomware :** Utilisation de qTox et d'adresses Protonmail, parfois explicitement sous le nom "Warlock Group".
*   **Fuite de Données :** Les victimes sont listées sur un site dédié sur le dark web, avec menace de publication des données ou de revente.
*   **Victimologie :** Cible divers secteurs, avec une concentration notable dans l'IT, l'industrie et la technologie. Des indices suggèrent un possible lien avec des groupes chinois par la nature de certaines cibles et l'utilisation de technologies spécifiques.

**Vulnérabilités (CVEs non spécifiés dans l'article, mais le vecteur d'exploitation est clé) :**

*   Vulnérabilités SharePoint (utilisées pour l'accès initial).

**Recommandations :**

*   Évaluer la nécessité d'exposer les serveurs SharePoint à Internet.
*   S'assurer que les serveurs exposés sur Internet sont correctement patchés.
*   Déployer largement des solutions antivirus (AV) et de détection et réponse d'end point (EDR) pour détecter l'activité à un stade précoce.
*   Surveiller les indicateurs de compromission (IoCs) fournis, tels que les noms de fichiers, domaines, URLs et hachages.

---
[Source](https://news.sophos.com/en-us/2025/12/11/gold-salem-tradecraft-for-deploying-warlock-ransomware/){:target="_blank"}
