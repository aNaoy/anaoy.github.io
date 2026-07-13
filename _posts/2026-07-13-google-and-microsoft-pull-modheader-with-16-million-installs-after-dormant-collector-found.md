---
title: 'Google and Microsoft Pull ModHeader With 1.6 Million Installs After Dormant Collector Found'
date: 2026-07-13
permalink: /posts/2026/07/13/google-and-microsoft-pull-modheader-with-16-million-installs-after-dormant-collector-found/
tags:
- veille-cyber
- hackernews
---
### Suppression de l'extension ModHeader : menace de collecte de données dormante

Google et Microsoft ont retiré l'extension populaire **ModHeader** (1,6 million d'utilisateurs) après la découverte d'un code malveillant intégré. Bien que dormant lors de sa détection, ce module était conçu pour collecter l'historique de navigation et exfiltrer les données via un serveur distant.

**Points clés :**
* **Méthodologie de dissimulation :** Le code malveillant utilisait une liste blanche vide pour rester inactif lors des analyses automatisées, rendant le comportement malveillant indétectable par les scanners de sécurité.
* **Mécanisme d'exfiltration :** L'extension créait une empreinte numérique de l'appareil, chiffrait les domaines visités et les envoyait quotidiennement vers un serveur externe (`api.stanfordstudies[.]com`).
* **Activités avérées :** L'extension communiquait activement avec `extensions-hub[.]com` et enregistrait localement des métadonnées de requêtes HTTP en texte clair.
* **Risque de détournement :** Le scénario confirme la tendance au rachat d'extensions légitimes par des acteurs malveillants pour transformer des outils de confiance en vecteurs de vol de données.

**Vulnérabilités :**
* Absence de CVE spécifique identifiée, mais le risque repose sur l'exploitation de permissions légitimes pour un usage détourné (collecte de données sans consentement).
* L'extension stockait localement des en-têtes HTTP complets, exposant des jetons d'authentification et des clés API en clair sur le disque de l'utilisateur.

**Recommandations :**
* **Utilisateurs :** Désinstallez immédiatement l'extension ModHeader. Si vous l'utilisiez pour gérer des jetons, clés API ou cookies de session, **révoquez et remplacez immédiatement ces secrets**, car ils ont pu être compromis.
* **Administrateurs/Défenseurs :** Bloquez les domaines `stanfordstudies[.]com` et `extensions-hub[.]com` au niveau des pare-feu et des serveurs DNS.
* **Surveillance :** Inspectez les journaux de sécurité à la recherche d'appels vers l'URL d'exfiltration (`api.stanfordstudies[.]com/app/log`) en utilisant des outils de chasse (KQL/SIEM).

---
[Source](https://thehackernews.com/2026/07/google-and-microsoft-pull-modheader.html){:target="_blank"}
