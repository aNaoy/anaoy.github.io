---
title: 'Scanning Webserver with /&#x24;(pwd)/ as a Starting Path, (Sun, Jan 25th)'
date: 2026-01-26
permalink: /posts/2026/01/26/scanning-webserver-with-x24pwd-as-a-starting-path-sun-jan-25th/
tags:
- veille-cyber
- sans-isc
---
**Campagne de Balayage de Serveurs Web Ciblant une Vulnérabilité Spécifique**

Une campagne d'exploration de serveurs web, détectée depuis le 13 janvier 2026 et observée plus largement à partir du 21 janvier 2026, cible une vulnérabilité particulière. Les attaquants utilisent le motif `/$(pwd)/` lors de leurs requêtes pour identifier des failles potentielles. L'analyse des logs suggère que deux adresses IP sont principalement impliquées dans ces scans.

**Points Clés :**

*   **Motif de Scan :** Les acteurs malveillants recherchent spécifiquement la séquence `/$(pwd)/`.
*   **Outils Potentiels :** La nature exacte de l'outil utilisé pour ces scans est sujette à investigation.
*   **Période d'Activité :** Les scans ont débuté mi-janvier 2026.

**Vulnérabilités :**

Aucune vulnérabilité spécifique avec un identifiant CVE n'est explicitement mentionnée dans l'article. L'utilisation du motif `/$(pwd)/` suggère une tentative d'exploitation de vulnérabilités liées à l'injection de commandes ou à des problèmes de traversée de répertoire (directory traversal), où la commande `pwd` (print working directory) est exécutée dans un contexte non sécurisé.

**Recommandations :**

Bien que l'article ne détaille pas de recommandations directes, les actions suivantes sont implicitement conseillées pour se prémunir contre ce type d'attaques :

*   **Surveillance des Logs :** Mettre en place une surveillance active des journaux du serveur web pour détecter la présence du motif `/$(pwd)/` ou des requêtes suspectes similaires.
*   **Analyse des Requêtes :** Examiner attentivement les requêtes HTTP qui utilisent des séquences inhabituelles ou des commandes potentielles dans leurs chemins ou paramètres.
*   **Mise à Jour et Patching :** S'assurer que les serveurs web et toutes les applications associées sont régulièrement mis à jour pour corriger les vulnérabilités connues qui pourraient permettre l'exécution de commandes ou la traversée de répertoire.
*   **Configuration Sécurisée :** Vérifier la configuration du serveur web pour s'assurer qu'elle ne permet pas l'exécution de commandes arbitraires via des requêtes malveillantes.
*   **Intrusion Detection/Prevention Systems (IDS/IPS) :** Configurer les systèmes de détection et de prévention d'intrusion pour identifier et bloquer les tentatives d'exploitation de ce type de vulnérabilité.

---
[Source](https://isc.sans.edu/diary/rss/32654){:target="_blank"}
