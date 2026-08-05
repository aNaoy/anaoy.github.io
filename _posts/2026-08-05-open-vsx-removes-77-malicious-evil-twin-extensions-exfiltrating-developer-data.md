---
title: 'Open VSX Removes 77 Malicious Evil Twin Extensions Exfiltrating Developer Data'
date: 2026-08-05
permalink: /posts/2026/08/05/open-vsx-removes-77-malicious-evil-twin-extensions-exfiltrating-developer-data/
tags:
- veille-cyber
- hackernews
---
### Campagne d'extensions malveillantes sur Open VSX

Soixante-dix-sept extensions malveillantes ont été supprimées du dépôt Open VSX après avoir été identifiées comme des « jumeaux maléfiques » (« evil twins ») imitant des outils de développement légitimes. Ces paquets, publiés entre fin juillet et début août 2026, visaient à exfiltrer des données sensibles des environnements de travail des développeurs vers un domaine unique (`mangorbit[.]com`).

#### Points clés
*   **Technique d'imitation :** Les attaquants ont usurpé le nom, l'espace de noms et la description d'extensions populaires de la marketplace VS Code, tout en utilisant des numéros de version bas (0.0.1).
*   **Nature de l'exfiltration :** 
    *   **Extensions légères :** Capture simple du nom d'hôte et de la version de l'éditeur.
    *   **Extensions de reconnaissance :** Collecte exhaustive incluant le système d'exploitation, les chemins de fichiers, les variables d'environnement CI (Azure, GitHub, CircleCI), les configurations Git, et les tokens d'accès.
*   **Persistance :** Le code malveillant inclut un mécanisme de nouvelle tentative (retry) s'étalant sur sept jours et une option de repli via DNS TXT en cas de blocage du domaine principal.
*   **Contexte global :** Cette menace s'inscrit dans un climat de cyberattaques accrues sur la chaîne d'approvisionnement logicielle, rappelant la compromission récente de paquets npm via le ver « ChainDrop ».

#### Vulnérabilités
Bien qu'aucune CVE spécifique ne soit associée à cette campagne (il s'agit d'une exploitation de la confiance dans les dépôts d'extensions), le risque repose sur :
*   **L'absence de contrôle granulaire des permissions** des extensions au sein des éditeurs de code.
*   **Le manque de validation stricte** lors de la publication sur les marketplaces de logiciels tiers.

#### Recommandations
*   **Vérification de l'éditeur :** Avant d'installer une extension, vérifier systématiquement l'identité du compte de l'éditeur et la cohérence du nombre de téléchargements.
*   **Audit des extensions installées :** Supprimer les extensions suspectes ou dont l'utilité ne semble pas correspondre à la description officielle.
*   **Isolation et permissions :** Limiter les privilèges des outils de développement et surveiller les communications réseau sortantes depuis l'environnement de travail.
*   **Renforcement de la sécurité CI/CD :** Appliquer des contrôles stricts sur les variables d'environnement et les accès utilisés dans les pipelines de déploiement pour limiter l'impact d'une exfiltration potentielle.

---
[Source](https://thehackernews.com/2026/08/open-vsx-removes-77-malicious-evil-twin.html){:target="_blank"}
