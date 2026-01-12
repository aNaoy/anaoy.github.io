---
title: 'Max severity Ni8mare flaw impacts nearly 60,000 n8n instances'
date: 2026-01-12
permalink: /posts/2026/01/12/max-severity-ni8mare-flaw-impacts-nearly-60000-n8n-instances/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilité Critique dans n8n : Risque pour les Instances Non Patchées

Une faille de sécurité critique, surnommée "Ni8mare", affecte près de 60 000 instances en ligne de n8n, une plateforme open-source d'automatisation de flux de travail. Cette vulnérabilité permet à des attaquants non authentifiés de prendre le contrôle des instances n8n déployées localement après avoir accédé aux fichiers du serveur sous-jacent. Étant donné que n8n centralise souvent des informations sensibles telles que des clés API, des jetons OAuth, des identifiants de bases de données et des secrets CI/CD, les instances compromises constituent une cible attrayante pour les acteurs malveillants.

**Points Clés :**

*   **Impact :** Environ 59 558 instances n8n exposées en ligne ne sont pas encore corrigées face à cette faille.
*   **Fonctionnalité n8n :** Permet d'automatiser des tâches répétitives en connectant diverses applications et services via une interface visuelle, souvent utilisée dans le développement d'IA pour l'ingestion de données et la création d'agents IA et de pipelines RAG.
*   **Risques pour les Attaquants :** Vol d'informations stockées sur le système, falsification de cookies de session pour contourner l'authentification, injection de fichiers sensibles dans les flux de travail, voire exécution de commandes arbitraires.

**Vulnérabilités :**

*   **Nom :** Ni8mare
*   **Identifiant CVE :** CVE-2026-21858
*   **Cause :** Une faiblesse d'improper input validation (validation incorrecte des entrées) due à une confusion du type de contenu lors de l'analyse des données par n8n.
*   **Conditions d'Exploitation :** Une instance n8n est potentiellement vulnérable si elle possède un flux de travail actif avec un déclencheur de soumission de formulaire acceptant un élément de fichier et un nœud de fin de formulaire renvoyant un fichier binaire.

**Recommandations :**

*   **Mise à Jour Immédiate :** Mettre à jour les instances n8n vers la version 1.121.0 ou ultérieure dès que possible.
*   **Solutions de Contournement (si la mise à jour n'est pas immédiate) :** Restreindre ou désactiver les points d'accès aux webhooks et formulaires publiquement accessibles.
*   **Analyse des Flux de Travail :** Utiliser le modèle de flux de travail fourni par l'équipe n8n pour scanner les instances à la recherche de flux potentiellement vulnérables.

---
[Source](https://www.bleepingcomputer.com/news/security/max-severity-ni8mare-flaw-impacts-nearly-60-000-n8n-instances/){:target="_blank"}
