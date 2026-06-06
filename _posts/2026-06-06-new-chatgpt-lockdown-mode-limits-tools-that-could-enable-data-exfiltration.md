---
title: 'New ChatGPT Lockdown Mode Limits Tools That Could Enable Data Exfiltration'
date: 2026-06-06
permalink: /posts/2026/06/06/new-chatgpt-lockdown-mode-limits-tools-that-could-enable-data-exfiltration/
tags:
- veille-cyber
- hackernews
---
### Sécurisation de ChatGPT : Introduction du « Lockdown Mode »

OpenAI déploie un nouveau mode « Lockdown » (verrouillage) pour ses abonnés ChatGPT afin de limiter les risques d'exfiltration de données causés par des attaques par injection de prompt. Ce paramètre optionnel renforce la sécurité en restreignant les capacités de connexion réseau du modèle vers l'extérieur.

**Points clés :**
* **Objectif :** Réduire la surface d'attaque en limitant les requêtes réseau sortantes que des attaquants pourraient exploiter pour exfiltrer des données sensibles.
* **Disponibilité :** Accessible aux utilisateurs Free, Go, Plus, Pro et Business.
* **Compatibilité :** Le mode Lockdown est incompatible avec le « Developer Mode » ; l'activation de l'un désactive automatiquement l'autre.
* **Limites :** Ce mode ne supprime pas le risque d'injection de prompt (le comportement du modèle peut toujours être altéré), mais il bloque les vecteurs de sortie de données.

**Vulnérabilités ciblées :**
* **Attaques par injection de prompt :** Risque persistant où une instruction malveillante manipule l'IA pour effectuer des actions non autorisées.
* **Exfiltration de données via URL :** Utilisation de requêtes réseau pour envoyer des données vers des serveurs contrôlés par des attaquants.
* *Note : Aucune CVE spécifique n'est mentionnée, le problème étant lié à la nature structurelle des LLM.*

**Fonctionnalités désactivées en mode Lockdown :**
* Navigation web en direct (accès limité aux contenus mis en cache).
* Affichage et récupération d'images sur le web.
* Outils de recherche approfondie (« Deep research ») et mode Agent.
* Accès réseau pour le code généré via Canvas.
* Téléchargement de fichiers pour l'analyse de données.

**Recommandations :**
* **Utilisation ciblée :** Activer ce mode uniquement pour les flux de travail manipulant des données hautement sensibles, compte tenu de la perte de fonctionnalités utiles.
* **Gestion des sessions :** Utiliser la nouvelle interface de gestion des sessions d'OpenAI pour surveiller et déconnecter régulièrement tout appareil suspect ou non reconnu.
* **Vigilance persistante :** Garder à l'esprit que le mode ne protège pas contre les manipulations de comportement induites par des fichiers malveillants, malgré les restrictions réseau.

---
[Source](https://thehackernews.com/2026/06/new-chatgpt-lockdown-mode-limits-tools.html){:target="_blank"}
