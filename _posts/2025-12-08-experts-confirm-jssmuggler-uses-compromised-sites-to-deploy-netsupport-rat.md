---
title: 'Experts Confirm JS#SMUGGLER Uses Compromised Sites to Deploy NetSupport RAT'
date: 2025-12-08
permalink: /posts/2025/12/08/experts-confirm-jssmuggler-uses-compromised-sites-to-deploy-netsupport-rat/
tags:
- veille-cyber
- hackernews
---
## JS#SMUGGLER : Une Campagne d'Infection Sophistiquée

Une nouvelle campagne de cybercriminalité, nommée JS#SMUGGLER, utilise des sites web compromis pour distribuer le logiciel malveillant NetSupport RAT. Cette opération malveillante repose sur une chaîne d'attaque en plusieurs étapes impliquant un chargeur JavaScript obfusqué injecté sur le site, une application HTML (HTA) qui exécute des "stagers" PowerShell cryptés via "mshta.exe", et enfin une charge utile PowerShell téléchargeant et exécutant le malware principal. NetSupport RAT offre aux attaquants un contrôle total sur la machine victime, permettant l'accès à distance, la manipulation de fichiers, l'exécution de commandes, le vol de données et des capacités de proxy.

Les chercheurs ne lient pas encore cette campagne à un groupe de menace spécifique, mais sa méthode de diffusion sur des sites web piratés suggère une approche à large échelle visant les utilisateurs d'entreprises. La technique emploie des iframes cachés, des chargeurs obfusqués et une exécution de scripts en couches pour déployer le malware et assurer le contrôle à distance.

Les techniques d'évasion incluent des redirections silencieuses, un chargeur JavaScript obfusqué ("phone.js") qui profile l'appareil pour adapter le chemin d'infection (iframe plein écran sur mobile, script de second niveau sur desktop), limitant ainsi les détections. L'exécution de la charge utile se fait de manière furtive, avec des étapes pour effacer les traces forensiques. La sophistication de ces méthodes suggère un cadre malveillant professionnellement maintenu.

Points Clés :

*   **Méthode de Distribution :** Utilisation de sites web compromis.
*   **Malware Principal :** NetSupport RAT (Remote Access Trojan).
*   **Techniques d'Attaque :** Iframes cachés, chargeurs JavaScript obfusqués, exécution de scripts en plusieurs étapes, redirection silencieuse.
*   **Vector d'Exécution :** JavaScript, HTA (via mshta.exe), PowerShell.
*   **Objectif du Malware :** Contrôle total de la machine victime.
*   **Évasion :** Adaptation à l'appareil, exécution en mémoire, effacement des traces.

Vulnérabilités (non spécifiées avec CVE) :

*   Les vulnérabilités exploitées résident dans la capacité à injecter du code malveillant sur des sites web, et l'exécution non restreinte de scripts et d'applications via des mécanismes comme `mshta.exe`. La confiance implicite dans le contenu web et la gestion des privilèges d'exécution jouent un rôle.

Recommandations :

*   Mise en place d'une application stricte de la politique de sécurité du contenu (CSP).
*   Surveillance des scripts et des activités PowerShell.
*   Restrictions sur l'utilisation de `mshta.exe`.
*   Utilisation d'analyses comportementales pour détecter les attaques.

---
[Source](https://thehackernews.com/2025/12/experts-confirm-jssmuggler-uses.html){:target="_blank"}
