---
title: 'ShinyHunters hackers claim breach of Florida "DAVID" DMV database'
date: 2026-09-08
permalink: /posts/2026/09/08/shinyhunters-hackers-claim-breach-of-florida-david-dmv-database/
tags:
- veille-cyber
- bleepingcomp
---
### Violation de la base de données DAVID de Floride par ShinyHunters

Le groupe de cybercriminels ShinyHunters affirme avoir compromis la plateforme DAVID (*Driver and Vehicle Information Database*) du département des véhicules motorisés (FLHSMV) de Floride. L'attaque aurait permis le vol de plus de 200 000 dossiers de conducteurs, incluant des informations sensibles telles que les adresses, numéros de sécurité sociale, dates de naissance et détails sur les véhicules.

**Points clés :**
* **Vecteur d'attaque :** Utilisation d'une faille dans le processus de réinitialisation de mot de passe du système.
* **Impact :** Accès aux comptes d'employés du DMV et d'un agent du FBI, permettant l'extraction massive de données depuis le 3 septembre.
* **Mode opératoire :** Après avoir obtenu des accès valides, les attaquants ont parcouru les enregistrements par ID pour télécharger les fichiers associés.
* **Statut actuel :** Les attaquants affirment avoir perdu l'accès au système et que la vulnérabilité est en cours de correction.
* **Contexte :** Le groupe a confirmé cibler d'autres DMV à travers les États-Unis via des techniques d'ingénierie sociale (vishing).

**Vulnérabilités :**
* Aucune CVE spécifique n'est mentionnée, mais le problème identifié est une **faille de logique métier dans la fonction de réinitialisation de mot de passe**, permettant une compromission de comptes à grande échelle.

**Recommandations :**
* **Sécurisation des processus d'authentification :** Auditer les mécanismes de réinitialisation de mot de passe pour prévenir toute usurpation.
* **Mise en œuvre du MFA robuste :** Renforcer l'authentification multifacteur pour contrer le vol de jetons de session et les attaques par "vishing" (phishing vocal).
* **Surveillance des accès :** Implémenter des outils de détection d'anomalies sur les comportements des utilisateurs (notamment pour détecter les itérations massives sur des bases de données).
* **Principe du moindre privilège :** Restreindre strictement les accès aux bases de données gouvernementales aux seules opérations nécessaires pour chaque profil utilisateur.

---
[Source](https://www.bleepingcomputer.com/news/security/shinyhunters-hackers-claim-breach-of-florida-david-dmv-database/){:target="_blank"}
