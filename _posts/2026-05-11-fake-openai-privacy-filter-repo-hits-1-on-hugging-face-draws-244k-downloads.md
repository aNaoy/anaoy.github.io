---
title: 'Fake OpenAI Privacy Filter Repo Hits #1 on Hugging Face, Draws 244K Downloads'
date: 2026-05-11
permalink: /posts/2026/05/11/fake-openai-privacy-filter-repo-hits-1-on-hugging-face-draws-244k-downloads/
tags:
- veille-cyber
- hackernews
---
### Menace sur les modèles IA : Un faux dépôt Hugging Face distribue des infostealers

Un dépôt malveillant sur Hugging Face, se faisant passer pour le "Privacy Filter" d'OpenAI, a attiré 244 000 téléchargements en se hissant en tête des tendances. Ce dépôt contenait un malware Rust conçu pour dérober des données sensibles.

**Points clés :**
*   **Tactique de tromperie :** Le dépôt utilisait le typosquatting et copiait fidèlement la documentation officielle d'OpenAI pour gagner la confiance des utilisateurs.
*   **Infection multi-étapes :** L'exécution d'un script (`loader.py` ou `start.bat`) déclenche une chaîne d'infection via PowerShell, téléchargeant un binaire malveillant qui désactive les protections Windows (Antivirus, AMSI, ETW).
*   **Objectif du malware :** Un infostealer dérobe des captures d'écran, des portefeuilles de cryptomonnaies, des identifiants (Discord, navigateurs) et des fichiers de configuration.
*   **Infrastructure liée :** L'enquête a révélé six autres dépôts suspects ainsi qu'un lien avec le groupe de cybercriminalité chinois "Silver Fox", déjà connu pour distribuer le cheval de Troie d'accès distant (RAT) nommé *ValleyRAT*.

**Vulnérabilités et vecteurs d'attaque :**
*   **Aucune CVE spécifique :** Cette attaque repose sur l'ingénierie sociale et l'exploitation de la confiance accordée aux plateformes de partage de modèles IA.
*   **Vecteur d'accès initial :** Empoisonnement des résultats de recherche et manipulation artificielle des compteurs de téléchargements/likes sur les plateformes open-source.

**Recommandations :**
*   **Vérification systématique :** Avant de télécharger un modèle ou un script, validez toujours l'identité de l'auteur et la cohérence de l'URL du dépôt avec les sources officielles.
*   **Analyse du code :** Inspectez les scripts de chargement (`loader.py`, `start.bat`) avant exécution, surtout s'ils nécessitent des privilèges élevés (UAC) ou effectuent des requêtes réseau non justifiées.
*   **Prudence avec les tendances :** Ne vous fiez pas au classement "trending" d'une plateforme, car celui-ci peut être manipulé artificiellement pour accroître la légitimité d'un contenu malveillant.
*   **Isolation :** Exécutez des modèles ou des scripts provenant de sources tierces dans des environnements isolés (sandboxes ou machines virtuelles) pour limiter l'exposition de votre système principal.

---
[Source](https://thehackernews.com/2026/05/fake-openai-privacy-filter-repo-hits-1.html){:target="_blank"}
