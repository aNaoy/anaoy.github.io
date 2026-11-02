---
title: 'Government Linux Servers Targeted With SysGoRAT and Suspected AI-Generated Scripts'
date: 2026-11-02
permalink: /posts/2026/11/02/government-linux-servers-targeted-with-sysgorat-and-suspected-ai-generated-scripts/
tags:
- veille-cyber
- hackernews
---
### Campagne d'espionnage Linux : Utilisation de l'IA et du malware SysGoRAT

Une campagne d'espionnage nommée **CL-UNK-1211**, active entre octobre 2025 et avril 2026, cible les infrastructures Linux gouvernementales. Les attaquants se distinguent par l'utilisation massive d'outils d'intelligence artificielle pour générer des scripts malveillants et automatiser leurs opérations, augmentant ainsi la vélocité de leurs attaques.

#### Points clés
*   **Automatisation par l'IA :** Les attaquants utilisent des modèles de langage (LLM) et des agents IA pour produire des scripts PHP et shell. La présence de notes de raisonnement dans le code suggère une génération directe via des prompts.
*   **SysGoRAT :** Un cheval de Troie d'accès distant (RAT) multiplateforme écrit en Go, capable d'établir une persistance, d'exécuter des commandes arbitraires, de prendre des captures d'écran et de servir de proxy pour exfiltrer des données.
*   **Tactiques de dissimulation :** Tentatives de suppression des logs système, désactivation des protections EDR et insertion de faux marqueurs "red-team" pour se faire passer pour des tests de sécurité légitimes.
*   **Vecteurs d'exfiltration :** Cible prioritaire sur les boîtes mail gouvernementales et les accès aux réseaux sociaux, avec des scripts dédiés à la recherche de mots-clés et à la compression des données.

#### Vulnérabilités exploitées
Bien qu'aucune CVE spécifique ne soit citée, les techniques d'accès reposent sur :
*   **Compromission de configuration :** Modification des fichiers `.bashrc` pour capturer les mots de passe.
*   **Injection de code :** Injection dans les pages de connexion PHP pour le vol de jetons d'administration.
*   **Mauvaises pratiques :** Recherche de mots de passe en clair dans les fichiers de configuration, l'historique des commandes et les répertoires de messagerie (`/var/qmail/mailnames/`).

#### Recommandations
*   **Surveillance accrue :** Auditer les fichiers de configuration système (comme `.bashrc`) et les répertoires web pour détecter des injections de code non autorisées.
*   **Analyse comportementale :** Détecter les connexions WebSocket suspectes vers des adresses IP inconnues et surveiller l'exécution de scripts présentant des structures de code "conversationnelles" typiques des sorties d'IA.
*   **Gestion des accès :** Appliquer le principe du moindre privilège sur les répertoires sensibles et chiffrer les informations d'identification stockées dans les fichiers de configuration.
*   **Vigilance sur les outils d'IA :** Être conscient de l'utilisation croissante de frameworks offensifs (type ARTEX) qui automatisent la reconnaissance et l'exploitation à une vitesse industrielle, rendant la détection rapide des anomalies réseau indispensable.

---
[Source](https://thehackernews.com/2026/11/government-linux-servers-targeted-with.html){:target="_blank"}
