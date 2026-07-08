---
title: 'Rogue Agent Flaw Could Have Let Attackers Hijack Google Dialogflow CX Chatbots'
date: 2026-07-08
permalink: /posts/2026/07/08/rogue-agent-flaw-could-have-let-attackers-hijack-google-dialogflow-cx-chatbots/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique "Rogue Agent" dans Google Dialogflow CX

Une faille de sécurité majeure, baptisée **"Rogue Agent"**, permettait à un attaquant disposant de droits d'édition sur un agent Dialogflow CX de prendre le contrôle de tous les autres agents partageant le même projet Google Cloud. Cette vulnérabilité, découverte par Varonis, exploitait l'absence d'isolation dans l'environnement d'exécution des "Code Blocks" (scripts Python personnalisés).

**Points clés :**
* **Vecteur d'attaque :** Nécessite la permission `dialogflow.playbooks.update`. Il ne s'agit pas d'une attaque externe anonyme, mais d'une menace liée à un accès interne compromis ou à un compte développeur malveillant.
* **Mécanisme :** Le fichier `code_execution_env.py` (chargé de l'exécution des scripts) était accessible en écriture dans l'environnement partagé. Un attaquant pouvait le remplacer par une version malveillante, interceptant ainsi les conversations, exfiltrant des données sensibles et injectant des messages (ex: phishing).
* **Fuites supplémentaires :** L'environnement d'exécution disposait d'un accès internet illimité (contournant les contrôles VPC) et permettait d'interroger le service de métadonnées (IMDS) pour potentiellement récupérer des jetons de service.
* **Absence de CVE :** Google a corrigé cette faille entre avril et juin 2026 sans qu'aucune CVE n'ait été assignée.

**Vulnérabilités identifiées :**
* **Défaut d'isolation logique :** Partage d'un environnement d'exécution non sécurisé entre plusieurs agents.
* **Manipulation de fichiers système :** Accès en écriture sur les fichiers de configuration de l'environnement Python.
* **Exfiltration de données :** Accès sortant non restreint vers internet.
* **Exposition de métadonnées :** Accès possible au service IMDS depuis le sandbox.

**Recommandations :**
* **Audit des accès :** Examiner rigoureusement les comptes et rôles possédant la permission `dialogflow.playbooks.update`.
* **Analyse des logs :** Rechercher dans les logs d'audit `DATA_WRITE` toute activité suspecte ou mise à jour non autorisée de "Playbooks".
* **Inspection des agents :** Vérifier, dans la console Dialogflow, que chaque "Code Block" configuré dans vos agents est bien légitime et approuvé.
* **Surveillance des erreurs :** Analyser les logs Cloud à la recherche d'exceptions inhabituelles pouvant indiquer l'exécution de code malveillant.

---
[Source](https://thehackernews.com/2026/07/rogue-agent-flaw-could-have-let.html){:target="_blank"}
