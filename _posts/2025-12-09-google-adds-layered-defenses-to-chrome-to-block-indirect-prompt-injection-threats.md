---
title: 'Google Adds Layered Defenses to Chrome to Block Indirect Prompt Injection Threats'
date: 2025-12-09
permalink: /posts/2025/12/09/google-adds-layered-defenses-to-chrome-to-block-indirect-prompt-injection-threats/
tags:
- veille-cyber
- hackernews
---
**Chrome Renforce sa Sécurité face aux Exploitations par Injection de Prompts Indirects**

Google introduit de nouvelles mesures de sécurité dans son navigateur Chrome pour contrer les risques d'attaques par injection de prompts indirects, une vulnérabilité souvent liée à l'exposition à des contenus web non fiables et à l'utilisation de capacités d'intelligence artificielle (IA) dans le navigateur.

**Points Clés et Vulnérabilités Potentielles :**

*   **Injection de Prompts Indirects :** Des acteurs malveillants peuvent manipuler des prompts afin que l'IA du navigateur exécute des actions non désirées par l'utilisateur, comme l'exfiltration de données ou la prise de contrôle d'actions légitimes.
*   **Bypass d'Isolement de Site :** Une IA compromise pourrait potentiellement interagir avec n'importe quel site web, y compris ceux où l'utilisateur est connecté, permettant l'exfiltration de données sensibles.
*   **Exécution d'Actions sans Confirmation :** La capacité pour un attaquant de faire exécuter des actions sans consentement utilisateur clair.
*   **Exfiltration de Données Sensibles :** Le vol d'informations confidentielles sans que l'utilisateur ait eu la possibilité de l'approuver.
*   **Contournement des Protections Existantes :** Les nouvelles mesures visent à empêcher que les protections actuelles ne soient inefficaces face à ces attaques.

**Recommandations et Nouvelles Fonctionnalités de Sécurité :**

*   **Critère d'Alignement Utilisateur (User Alignment Critic) :** Un second modèle évalue indépendamment les actions proposées par l'IA, isolé des prompts potentiellement malveillants, afin de s'assurer qu'elles correspondent aux objectifs de l'utilisateur. Il ne peut pas accéder au contenu web non fiable.
*   **Ensembles d'Origines d'Agents (Agent Origin Sets) :** L'agent n'a accès qu'aux données provenant d'origines pertinentes pour la tâche ou explicitement partagées par l'utilisateur. Cette restriction est mise en œuvre par une fonction de filtrage distinguant les origines en lecture seule et en lecture/écriture pour limiter les vecteurs de fuite de données inter-sites.
*   **Transparence et Contrôle Utilisateur :** L'agent génère un journal d'activités et demande une approbation explicite avant d'accéder à des sites sensibles (banques, santé), de se connecter via le gestionnaire de mots de passe, ou d'effectuer des actions comme des achats ou des envois de messages.
*   **Détection de Prompts Malveillants :** Un classificateur vérifie chaque page à la recherche d'injections de prompts, fonctionnant en parallèle avec les protections existantes comme la Navigation Sécurisée et la détection d'arnaques sur l'appareil.
*   **Programme de Récompenses :** Google offre des récompenses allant jusqu'à 20 000 $ pour les démonstrations de failles exploitant les nouvelles protections de sécurité.

Ces mesures s'inscrivent dans une approche de défense en couches et de confiance dans l'architecture des modèles pour sécuriser les expériences d'IA agentiques dans Chrome.

---
[Source](https://thehackernews.com/2025/12/google-adds-layered-defenses-to-chrome.html){:target="_blank"}
