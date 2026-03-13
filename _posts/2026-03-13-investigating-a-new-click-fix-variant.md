---
title: 'Investigating a New Click-Fix Variant'
date: 2026-03-13
permalink: /posts/2026/03/13/investigating-a-new-click-fix-variant/
tags:
- veille-cyber
- hackernews
---
### Évolution de la technique ClickFix : Abus de WebDAV et d'applications Electron

Une nouvelle variante de la technique d'attaque « ClickFix » a été identifiée. Elle repose sur l'ingénierie sociale pour inciter l'utilisateur à exécuter une commande malveillante via le menu « Exécuter » (Win + R) de Windows, permettant de contourner les protections classiques par une approche plus furtive.

**Points clés :**
*   **Vecteur initial :** Une page web imitant un mécanisme CAPTCHA demande à l'utilisateur de copier-coller une commande dans la boîte de dialogue « Exécuter ».
*   **Abus de protocole :** La commande utilise `net use` pour mapper un lecteur réseau distant via WebDAV. Un fichier batch (`update.cmd`) y est exécuté avant que le lecteur ne soit immédiatement démonté, effaçant ainsi les traces locales.
*   **Mécanisme de charge utile :** Le script télécharge une archive ZIP contenant une version obsolète de l'application légitime *WorkFlowy* (basée sur Electron). Le code malveillant est injecté dans le fichier `main.js` au sein de l'archive `app.asar`.
*   **Fonctionnalités malveillantes :** L'application trojanisée exécute un processus Node.js privilégié, établit une persistance via un identifiant unique stocké dans `%APPDATA%\id.txt`, et communique avec un serveur C2 toutes les deux secondes pour recevoir des instructions ou télécharger des charges utiles supplémentaires.
*   **Furtivité :** En utilisant le processus légitime d'une application Electron, l'attaquant opère en dehors de la sandbox Chromium, échappant aux solutions EDR qui inspectent rarement les fichiers `.asar`.

**Vulnérabilités :**
*   **Abus de fonctionnalité légitime :** Le recours à `net use` pour monter des partages WebDAV permet de charger des scripts distants sans déclencher les alertes habituelles liées aux exécuteurs de scripts (PowerShell, MSHTA).
*   **Absence de CVE spécifique :** Cette attaque repose sur l'exploitation de comportements "Living-off-the-Land" (LotL) et de la confiance accordée aux applications signées, plutôt que sur une faille logicielle répertoriée par un CVE.

**Recommandations :**
*   **Détection proactive (Threat Hunting) :** Surveiller les entrées de registre `RunMRU` (historique du menu Exécuter) via les logs EDR/Sysmon. Une recherche sur l'exécution de commandes suspectes (`net.exe`, `cmd.exe`, etc.) initiées par `explorer.exe` est recommandée.
*   **Sécurisation du réseau :** Restreindre les communications sortantes vers les serveurs WebDAV externes non approuvés au niveau du pare-feu.
*   **Analyse des endpoints :** Mettre en œuvre des règles de détection comportementale axées sur le lancement d'applications Electron dont les archives `app.asar` ont été modifiées ou ne correspondent pas aux signatures de l'éditeur.
*   **Sensibilisation :** Éduquer les utilisateurs sur les risques liés au copier-coller de commandes provenant de sites web, même s'ils semblent légitimes.

---
[Source](https://thehackernews.com/2026/03/investigating-new-click-fix-variant.html){:target="_blank"}
