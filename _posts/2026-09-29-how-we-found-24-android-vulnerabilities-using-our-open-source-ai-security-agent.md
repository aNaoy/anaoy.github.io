---
title: 'How we found 24 Android vulnerabilities using our open source AI security agent'
date: 2026-09-29
permalink: /posts/2026/09/29/how-we-found-24-android-vulnerabilities-using-our-open-source-ai-security-agent/
tags:
- veille-cyber
- zerodaysfans
---
### Automatiser la recherche de vulnérabilités Android via l'IA

Le GitHub Security Lab a développé le **Security Lab Taskflow Agent**, un framework open source permettant d'automatiser l'audit de code via des modèles de langage (LLM). En guidant l'IA par des prompts ciblés, les chercheurs peuvent identifier des vulnérabilités complexes dans des applications Android que les méthodes d'analyse traditionnelles pourraient omettre.

#### Points clés
*   **Approche par étapes :** Le framework décompose l'analyse en étapes incrémentales (identification des points d'entrée, classification des vulnérabilités) pour améliorer la précision des LLM.
*   **Performance :** Plus de 20 vulnérabilités ont été découvertes et signalées en utilisant ces flux de travail automatisés.
*   **Limites actuelles :** Les LLM excellent dans la connaissance des API et des modèles d'attaques, mais peinent à évaluer la sévérité réelle des vulnérabilités, générant parfois des faux positifs nécessitant une vérification humaine.

#### Exemples de vulnérabilités découvertes
1.  **OsmAnd (Suivi de localisation) :** Une mauvaise gestion des *intents* exportés permettait à une application tierce d'injecter des paramètres arbitraires. Cela autorisait l'importation silencieuse de réglages malveillants, permettant à un attaquant de modifier les sources de tuiles cartographiques pour exfiltrer les coordonnées GPS et les historiques de navigation de l'utilisateur.
2.  **Wikipedia (Prise de contrôle de compte) :** Un bug de logique dans le parseur d'URL des *deeplinks* permettait de charger des pages web arbitraires en les faisant passer pour des domaines légitimes. En combinant cela avec une faille de gestion des cookies, un attaquant pouvait dérober des jetons de session persistants.

#### Recommandations
*   **Usage du framework :** Les développeurs et chercheurs peuvent utiliser le [seclab-taskflow-agent](https://github.com/GitHubSecurityLab/seclab-taskflow-agent) via GitHub Codespaces en utilisant la commande `./scripts/audit/run_mobile.sh`.
*   **Validation humaine :** Tout résultat fourni par l'IA doit impérativement être revu par un expert en sécurité pour confirmer l'exploitabilité réelle et écarter les faux positifs.
*   **Sécurisation Android :** Porter une attention particulière aux composants exportés (*activities*, *services*) et restreindre strictement les entrées provenant d'Intents externes. Éviter d'utiliser des paramètres contrôlables par l'utilisateur pour altérer des configurations critiques sans vérification.

---
[Source](https://github.blog/security/how-we-found-24-android-vulnerabilities-using-our-open-source-ai-security-agent/){:target="_blank"}
