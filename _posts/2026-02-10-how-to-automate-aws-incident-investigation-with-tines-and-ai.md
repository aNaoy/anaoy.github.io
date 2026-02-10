---
title: 'How to Automate AWS Incident Investigation with Tines and AI'
date: 2026-02-10
permalink: /posts/2026/02/10/how-to-automate-aws-incident-investigation-with-tines-and-ai/
tags:
- veille-cyber
- bleepingcomp
---
### Automatisation de l'investigation AWS grâce à l'IA et à des agents

Les alertes sur les infrastructures cloud, comme "Instance EC2 non réactive" ou "Utilisation CPU élevée", déclenchent souvent des investigations manuelles fastidieuses. Ces procédures impliquent de quitter le système de gestion des tickets, de se connecter à la console AWS, de rechercher la ressource spécifique et d'exécuter des commandes CLI. Cette surcharge contextuelle allonge le temps moyen de résolution (MTTR) et épuise les analystes.

Une solution proposée automatise la collecte de données en intégrant la ligne de commande (CLI) directement dans le processus d'investigation. Cette approche vise à éliminer le "fossé contextuel" entre les outils de suivi (Jira, ServiceNow) et les sources de données cloud (AWS).

**Points Clés :**

*   **Problème :** Le "fossé contextuel" dans la réponse aux incidents se traduit par des frictions d'accès (connexions multiples, rôles), des difficultés syntaxiques avec la CLI, et des risques de sécurité liés à des accès étendus aux environnements de production.
*   **Solution :** Un workflow Tines utilise des "agents" sécurisés et légers pour exécuter des commandes CLI sur AWS avec des identifiants spécifiques en lecture seule. Ces agents s'interfacent directement avec l'environnement cloud, sans que l'analyste ait besoin de s'y connecter.
*   **Fonctionnement du workflow :**
    1.  **Déclencheur :** Création d'un ticket concernant une ressource AWS.
    2.  **Agent :** Un agent Tines, doté d'un accès limité en lecture seule, reçoit les instructions.
    3.  **Génération dynamique de commandes :** L'agent construit la commande CLI appropriée en fonction du contexte du ticket (ex: politique de bucket S3, groupe de sécurité EC2).
    4.  **Traitement et Enrichissement par IA :** La sortie brute de la CLI est analysée et formatée en un résumé lisible ou un tableau, éventuellement à l'aide de l'IA.
    5.  **Mise à jour du Cas :** Les informations formatées sont directement ajoutées au ticket ou au système ITSM, offrant à l'analyste un aperçu immédiat sans nécessiter de connexion à la console.

**Avantages :**

*   **Contexte immédiat :** Les analystes disposent des données dès le début de l'investigation, passant directement à la phase de résolution.
*   **Accès sécurisé :** L'accès aux identifiants AWS est géré par l'agent, évitant de donner des permissions étendues aux analystes.
*   **Documentation standardisée :** Chaque investigation génère un historique de données cohérent, facilitant l'audit.
*   **Collaboration améliorée :** Les données centralisées dans les "Cas" Tines permettent une collaboration en temps réel.

**Mise en œuvre :**

Le workflow est disponible sous forme de modèle importable depuis la bibliothèque Tines. Après importation, il suffit de connecter un identifiant AWS sécurisé (rôle IAM ou clé d'accès) et de personnaliser les commandes recommandées selon les besoins spécifiques de l'équipe. La sortie est pré-configurée pour être envoyée aux "Cas" Tines, nécessitant une vérification du format de présentation des données.

**Recommandations :**

*   Utiliser le modèle "Investigate AWS issues with CLI data using agents" de la bibliothèque Tines.
*   Connecter un identifiant AWS sécurisé avec des permissions en lecture seule pour les agents.
*   Adapter la liste des commandes CLI exécutées par l'agent pour correspondre aux incidents les plus fréquents.
*   Vérifier et ajuster le format de présentation des résultats dans les "Cas" Tines pour une visibilité optimale.

L'adoption de workflows automatisés comme celui-ci permet de transformer la posture de sécurité en libérant les analystes des tâches répétitives et en leur permettant de se concentrer sur la prise de décision à haute valeur ajoutée.

---
[Source](https://www.bleepingcomputer.com/news/security/how-to-automate-aws-incident-investigation-with-tines-and-ai/){:target="_blank"}
