---
title: 'Fake LastPass Authenticator Installer Abuses Microsoft-Signed Driver to Kill Antivirus and EDR'
date: 2026-09-21
permalink: /posts/2026/09/21/fake-lastpass-authenticator-installer-abuses-microsoft-signed-driver-to-kill-antivirus-and-edr/
tags:
- veille-cyber
- hackernews
---
### Infiltration par un faux installateur LastPass : la menace du "Bring Your Own Vulnerable Driver" (BYOVD)

Une campagne malveillante utilise de fausses pages GitHub imitant LastPass pour distribuer un installeur vérolé. Une fois exécuté, celui-ci déploie un pilote noyau légitimement signé par Microsoft afin de désactiver les logiciels de sécurité (antivirus et EDR) avant de dérober des données sensibles.

**Points clés :**
*   **Technique BYOVD :** Les attaquants utilisent un pilote tiers légitime (nommé *CnCrypt/CcProtect.sys*, renommé *Alinubx.sys*), signé numériquement, pour contourner les protections Windows au niveau du noyau.
*   **Neutralisation des défenses :** Le pilote contient une liste de 145 processus de sécurité qu'il termine systématiquement dès le démarrage.
*   **Vol de données :** Une fois les défenses neutralisées, le logiciel malveillant (baptisé *Rapuncel*) extrait les mots de passe des navigateurs, les portefeuilles de cryptomonnaies, ainsi que les sessions Discord, Telegram et Steam.
*   **Persistance :** Le pilote se recharge à chaque redémarrage, garantissant que les outils de sécurité restent inactifs.

**Vulnérabilités :**
*   **Exploitation de la signature Microsoft :** Le pilote bénéficie d'une signature valide du programme de compatibilité matérielle de Microsoft, ce qui lui permet de passer outre les contrôles de sécurité. 
*   **Absence dans la liste de blocage :** Bien que connu sur des catalogues comme LOLDrivers, ce pilote spécifique ne figurait pas dans la liste de blocage officielle de Microsoft au moment de l'analyse, car les listes reposent souvent sur des hashes de fichiers précis, facilement contournables par un renommage ou une re-compilation.

**Recommandations :**
*   **Réaction en cas d'infection :** Considérer la machine comme compromise au niveau du noyau. Une réinstallation complète du système est fortement recommandée.
*   **Remédiation des comptes :** Modifier tous les mots de passe et réinitialiser les jetons de session (Discord, Telegram, etc.) depuis un appareil sain.
*   **Indicateurs de compromission (IoC) à surveiller :**
    *   Service créé sous le nom `NvFsFilter`.
    *   Présence du fichier `C:\Windows\System32\drivers
vfsflt64.sys`.
    *   Chemin de périphérique `\.\Alinubx`.
*   **Vigilance :** Ne télécharger des logiciels que depuis les sites officiels des éditeurs. Les résultats de recherche Google affichant des dépôts GitHub non officiels doivent être traités avec une extrême méfiance.

---
[Source](https://thehackernews.com/2026/09/fake-lastpass-authenticator-installer.html){:target="_blank"}
