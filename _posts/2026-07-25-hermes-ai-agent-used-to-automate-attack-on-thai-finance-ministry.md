---
title: 'Hermes AI agent used to automate attack on Thai Finance Ministry'
date: 2026-07-25
permalink: /posts/2026/07/25/hermes-ai-agent-used-to-automate-attack-on-thai-finance-ministry/
tags:
- veille-cyber
- bleepingcomp
---
### Automatisation des cyberattaques : le cas du Ministère thaïlandais des Finances

Des chercheurs de Hunt.io ont découvert une infrastructure d'attaque exposée en ligne, révélant l'utilisation de l'agent IA open-source **Hermes** pour automatiser des activités de post-exploitation contre le Ministère thaïlandais des Finances. Les assaillants ont exploité le mode « YOLO » (You Only Look Once) de l'IA, qui permet à l'agent d'exécuter des commandes dangereuses sans intervention ni approbation humaine.

#### Points clés
*   **Mode opératoire :** L'agent Hermes a été utilisé pour automatiser l'énumération des services, la recherche de vulnérabilités noyau, l'inspection de conteneurs et l'utilisation de scripts d'élévation de privilèges (LinPEAS).
*   **Infrastructure exposée :** Des répertoires web non sécurisés contenaient des preuves de l'attaque : logs de l'IA, outils de tunnelisation HTTP, web shells PHP et un implant Go inédit nommé « Hades ».
*   **Cibles identifiées :** Les scripts visaient spécifiquement les infrastructures Hadoop, les consoles Apache Ambari et GlassFish, ainsi que les serveurs de messagerie du ministère.
*   **Portée de l'intrusion :** Bien que des données sensibles (documents RH, évaluations de performance) aient été cataloguées par l'IA, aucune preuve d'exfiltration massive n'a été confirmée à ce jour.

#### Vulnérabilités ciblées
Bien qu'aucune CVE spécifique n'ait été citée comme point d'entrée initial, l'attaque repose sur :
*   Des mauvaises configurations d'accès aux répertoires web (exposant l'infrastructure des attaquants).
*   L'utilisation de scripts d'énumération pour identifier des vulnérabilités locales sur les systèmes cibles.
*   La persistance de services administratifs vulnérables (Hadoop/Ambari/GlassFish) au sein du réseau interne.

#### Recommandations
*   **Sécurisation des accès :** Auditer rigoureusement les répertoires exposés et appliquer le principe du moindre privilège aux consoles d'administration (Hadoop, Ambari, GlassFish).
*   **Surveillance des logs IA :** Détecter les comportements atypiques liés à l'exécution automatisée de scripts système, particulièrement ceux utilisant des outils comme LinPEAS.
*   **Gestion des identités :** Renforcer les politiques de mots de passe pour prévenir les attaques par force brute contre les serveurs de messagerie.
*   **Surveillance des certificats :** Utiliser les empreintes JA4X pour identifier et corréler les serveurs faisant partie d'une même infrastructure malveillante.

---
[Source](https://www.bleepingcomputer.com/news/security/hermes-ai-agent-used-to-automate-attack-on-thai-finance-ministry/){:target="_blank"}
