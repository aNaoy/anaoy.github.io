---
title: 'China-Linked Hackers Use ARTEX AI Agents in ConnectWise Supply Chain Attack'
date: 2026-10-22
permalink: /posts/2026/10/22/china-linked-hackers-use-artex-ai-agents-in-connectwise-supply-chain-attack/
tags:
- veille-cyber
- hackernews
---
### Compromission de la chaîne d'approvisionnement ConnectWise par l'IA générative

Le groupe de hackers affilié à l'État chinois **Storm-0940** (également suivi sous le nom de TAG-217) a compromis l'application ConnectWise Cloud Backup. Les attaquants utilisent le framework d'IA agentique **ARTEX** pour automatiser et accélérer des attaques à grande échelle, notamment le *password spraying* et l'abus d'applications OAuth, permettant une escalade des privilèges en moins de trois heures.

**Points clés :**
* **Automatisation massive :** L'usage d'agents IA permet de mener des attaques à "vitesse machine" (plus de 2 900 tentatives de connexion par minute).
* **Mode opératoire :** Après avoir compromis les identifiants d'applications cloud, les attaquants utilisent la confiance établie de ces applications pour s'authentifier dans les environnements clients sans intervention humaine.
* **Persistance :** Les agents modifient les privilèges et ajoutent des identifiants aux applications OAuth existantes, assurant un accès pérenne même après la remédiation de la brèche initiale.
* **Cibles :** Large spectre incluant les secteurs de la défense, de l'énergie, de la finance, du gouvernement et de la technologie.

**Vulnérabilités :**
* Aucune CVE spécifique n'est mentionnée, car l'attaque repose sur l'abus de fonctionnalités légitimes d'applications (OAuth) et le vol d'identifiants via des techniques de *password spraying* automatisé.

**Recommandations :**
* **Audit OAuth :** Examiner régulièrement les applications OAuth autorisées dans l'infrastructure cloud et supprimer les permissions inutilisées ou suspectes.
* **Surveillance des accès :** Détecter les anomalies dans les journaux d'authentification (pics de tentatives infructueuses) et les modifications de privilèges sur les rôles administratifs.
* **Renforcement de l'authentification :** Appliquer une authentification multifacteur (MFA) robuste et restreindre les accès basés sur les jetons d'application.
* **Stratégie de défense :** Compte tenu de la vitesse d'exécution des agents IA, mettre en place des mécanismes de réponse automatisée pour bloquer les IP suspectes après un seuil prédéfini de tentatives d'échec.

---
[Source](https://thehackernews.com/2026/10/china-linked-hackers-use-artex-ai.html){:target="_blank"}
