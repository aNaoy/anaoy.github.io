---
title: 'MuddyWater Deploys UDPGangster Backdoor in Targeted Turkey-Israel-Azerbaijan Campaign'
date: 2025-12-08
permalink: /posts/2025/12/08/muddywater-deploys-udpgangster-backdoor-in-targeted-turkey-israel-azerbaijan-campaign/
tags:
- veille-cyber
- hackernews
---
**UDPGangster : Nouvelle campagne de cyberespionnage ciblée**

Le groupe de pirates informatiques iraniens MuddyWater utilise une nouvelle porte dérobée nommée UDPGangster, communiquant via le protocole UDP pour ses commandes et contrôles. Cette campagne d'espionnage vise spécifiquement des utilisateurs en Turquie, en Israël et en Azerbaïdjan.

La méthode d'attaque initiale repose sur le spear-phishing, utilisant des documents Microsoft Word piégés. Une fois les macros activées, un code malveillant s'exécute. Les messages d'hameçonnage usurpent l'identité du Ministère des Affaires Étrangères de la République Turque de Chypre du Nord, invitant les destinataires à un séminaire en ligne sur les élections présidentielles.

Le script VBA caché dans le document exécute la porte dérobée UDPGangster après avoir décodé des données. Ce malware est conçu pour échapper aux défenses réseau traditionnelles et dissimuler son activité, notamment en affichant une fausse image d'alerte de déconnexion du fournisseur israélien Bezeq.

UDPGangster cherche à établir une persistance sur les systèmes compromis et intègre des routines anti-analyse avancées pour déjouer les chercheurs en sécurité. Ces routines incluent la détection de débogueurs, l'analyse des environnements virtuels et des configurations système limitées, ainsi que la recherche d'outils d'analyse ou de machines virtuelles spécifiques.

Une fois ces vérifications passées, UDPGangster collecte des informations système, établit une connexion avec un serveur de commande et contrôle externe via le port UDP 1269 pour exfiltrer des données, exécuter des commandes, transmettre des fichiers, mettre à jour le serveur C2 et déployer des charges utiles supplémentaires.

**Points Clés:**

*   **Acteur de menace:** MuddyWater (groupe de pirates iraniens).
*   **Nouveau malware:** UDPGangster (porte dérobée).
*   **Protocole de communication:** UDP pour les commandes et contrôles (C2).
*   **Cibles:** Utilisateurs en Turquie, Israël et Azerbaïdjan.
*   **Méthode d'accès initiale:** Spear-phishing avec documents Word piégés et activation de macros.
*   **Fonctionnalités du malware:** Exécution de commandes à distance, exfiltration de fichiers, déploiement de charges utiles supplémentaires.
*   **Techniques anti-analyse:** Détection de débogage, analyse d'environnements virtuels, vérification de configuration système et de processus.
*   **Objectif:** Cyberespionnage.

**Vulnérabilités:**

*   L'article ne mentionne pas de CVE spécifiques exploitées par ce malware. L'accès initial repose sur l'ingénierie sociale (spear-phishing) et l'activation de macros par l'utilisateur, qui est une fonctionnalité légitime des documents Office. La vulnérabilité réside dans la confiance de l'utilisateur et la présence de macro potentiellement malveillantes.

**Recommandations:**

*   Faire preuve de prudence face aux documents non sollicités, particulièrement ceux demandant l'activation de macros.
*   Éduquer les utilisateurs sur les risques du spear-phishing et de l'activation de macros sur des documents suspects.
*   Maintenir les systèmes de sécurité à jour et utiliser des solutions capables de détecter les comportements suspects et les malwares.

---
[Source](https://thehackernews.com/2025/12/muddywater-deploys-udpgangster-backdoor.html){:target="_blank"}
