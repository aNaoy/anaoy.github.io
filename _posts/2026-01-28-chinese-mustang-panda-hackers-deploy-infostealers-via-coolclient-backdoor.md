---
title: 'Chinese Mustang Panda hackers deploy infostealers via CoolClient backdoor'
date: 2026-01-28
permalink: /posts/2026/01/28/chinese-mustang-panda-hackers-deploy-infostealers-via-coolclient-backdoor/
tags:
- veille-cyber
- bleepingcomp
---
### Évolution de CoolClient : une backdoor évoluée par Mustang Panda

Le groupe de hackers chinois Mustang Panda a mis à jour sa backdoor CoolClient avec de nouvelles fonctionnalités. Cette version améliorée est capable de voler des données de connexion des navigateurs web et de surveiller le presse-papiers. Les chercheurs de Kaspersky ont également noté que ce malware a été utilisé pour déployer un rootkit jusqu'alors inconnu.

CoolClient est utilisé par Mustang Panda depuis 2022, souvent en complément d'autres backdoors comme PlugX et LuminousMoth. Les récentes attaques ciblant des entités gouvernementales au Myanmar, en Mongolie, en Malaisie, en Russie et au Pakistan ont vu cette nouvelle variante déployée via des logiciels légitimes de la société chinoise Sangfor. Auparavant, le malware était distribué par le biais d'une technique de "DLL side-loading" exploitant des binaires signés de logiciels populaires tels que Bitdefender ou VLC Media Player.

La backdoor recueille des informations détaillées sur le système compromis, notamment le nom de l'ordinateur, la version du système d'exploitation, la mémoire vive, les informations réseau, ainsi que les descriptions et versions des pilotes chargés. La persistance est assurée par des modifications du registre, l'ajout de services Windows et la création de tâches planifiées. CoolClient est également capable de contourner l'UAC (User Account Control) et d'obtenir une élévation de privilèges.

Parmi les nouvelles capacités notables de CoolClient :

*   **Surveillance du presse-papiers** : Capture activement le contenu copié.
*   **Suivi des titres de fenêtres actives** : Permet de suivre l'application utilisée par l'utilisateur.
*   **Extraction de credentials HTTP proxy** : Analyse les paquets bruts et les en-têtes pour récupérer des informations d'identification.
*   **Fonctionnalités étendues des plugins** : Ajout d'un plugin de shell distant, d'un plugin de gestion des services et d'un plugin de gestion de fichiers plus performant (incluant la compression ZIP et le mappage de lecteurs réseau).
*   **Vol de données de navigateurs** : Des "infostealers" dédiés ont été développés pour voler les données de connexion des navigateurs Chrome, Edge et de tout navigateur basé sur Chromium.
*   **Exfiltration de données** : Utilisation de jetons d'API codés en dur pour des services légitimes comme Google Drive ou Pixeldrain pour faciliter l'exfiltration et échapper à la détection.

Mustang Panda continue de développer ses outils, ayant récemment utilisé un nouveau chargeur en mode noyau pour déployer une variante de la backdoor ToneShell. Le groupe est également identifié comme une menace majeure ciblant les infrastructures critiques, notamment à Taiwan.

**Points clés :**

*   Mustang Panda met à jour sa backdoor CoolClient.
*   La nouvelle variante vole des identifiants de navigateurs et surveille le presse-papiers.
*   Les cibles incluent des entités gouvernementales en Asie et en Europe de l'Est.
*   La distribution se fait via des logiciels légitimes de Sangfor.
*   La backdoor utilise des techniques de persistance avancées et d'élévation de privilèges.

**Vulnérabilités :**

*   Aucune vulnérabilité spécifique (CVE) n'est mentionnée dans l'article concernant CoolClient lui-même, mais les méthodes de déploiement exploitent des fonctionnalités légitimes des systèmes d'exploitation et des logiciels pour s'introduire.

**Recommandations :**

*   Maintenir les systèmes d'exploitation et les logiciels à jour pour atténuer les risques liés aux techniques d'exploitation courantes.
*   Renforcer la surveillance des activités suspectes sur le réseau et les points d'accès, notamment concernant l'installation de logiciels depuis des sources non fiables ou inattendues.
*   Utiliser des solutions de sécurité avancées capables de détecter les malwares et les comportements suspects, y compris les rootkits et les infostealers.
*   Sensibiliser les utilisateurs aux risques de phishing et à l'importance de vérifier la légitimité des logiciels téléchargés.

---
[Source](https://www.bleepingcomputer.com/news/security/chinese-mustang-panda-hackers-deploy-infostealers-via-coolclient-backdoor/){:target="_blank"}
