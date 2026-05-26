---
title: 'Possible ACR Stealer From Page Impersonating Claude, (Tue, May 26th)'
date: 2026-05-26
permalink: /posts/2026/05/26/possible-acr-stealer-from-page-impersonating-claude-tue-may-26th/
tags:
- veille-cyber
- sans-isc
---
### Propagation de malwares via des sites usurpant l'identité de Claude

Des campagnes malveillantes utilisent actuellement des publicités frauduleuses sur Google pour rediriger les utilisateurs vers de faux sites web imitant l'interface de l'IA Claude. Ces pages adaptent leur contenu en fonction du système d'exploitation de la victime (macOS ou Windows) pour proposer des instructions d'installation factices qui conduisent à l'exécution de malwares.

**Points clés :**
* **Infection identifiée :** Le logiciel malveillant distribué est identifié comme **ACR Stealer**, un programme conçu pour exfiltrer des données sensibles.
* **Chaîne d'infection :** Le processus repose sur le téléchargement successif de fichiers (archives ZIP, scripts PowerShell et images potentiellement utilisées pour masquer des charges utiles ou établir des connexions).
* **Vecteur initial :** Publicités malveillantes (malvertising) dans les résultats de recherche Google, utilisant parfois des redirections via des sous-domaines légitimes comme `sites.google.com`.

**Vulnérabilités :**
* Aucune CVE spécifique n'est mentionnée ; l'attaque repose sur l'ingénierie sociale poussant l'utilisateur à télécharger et exécuter volontairement des fichiers malveillants.

**Recommandations :**
* **Vérification des sources :** Téléchargez uniquement les logiciels depuis les sites officiels des éditeurs (ex: `claude.ai`).
* **Méfiance vis-à-vis des publicités :** Soyez vigilant face aux liens sponsorisés apparaissant en haut des résultats de recherche, qui sont fréquemment détournés pour diffuser des malwares.
* **Protection des terminaux :** Maintenez vos solutions de sécurité à jour et surveillez les connexions sortantes suspectes vers des domaines inconnus ou récents (ex: serveurs C2 comme `yw.enhanceblabber.cc`).
* **Analyse des téléchargements :** Évitez d'exécuter des fichiers provenant de sources non vérifiées ou de sites dont l'URL semble inhabituelle.

---
[Source](https://isc.sans.edu/diary/rss/33018){:target="_blank"}
