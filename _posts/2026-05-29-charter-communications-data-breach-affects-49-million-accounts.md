---
title: 'Charter Communications data breach affects 4.9 million accounts'
date: 2026-05-29
permalink: /posts/2026/05/29/charter-communications-data-breach-affects-49-million-accounts/
tags:
- veille-cyber
- bleepingcomp
---
### Violation de données chez Charter Communications : 4,9 millions de comptes exposés

Le géant américain des télécommunications Charter Communications a subi une cyberattaque menée par le groupe d'extorsion ShinyHunters, entraînant la compromission des informations personnelles de 4,9 millions de comptes. Bien que Charter minimise l'impact en affirmant qu'aucune donnée sensible ou information propriétaire (CPNI) n'a été exfiltrée, les analyses externes confirment la fuite de données massives.

**Points clés :**
*   **Vecteur d'attaque :** Utilisation du "vishing" (phishing vocal) pour compromettre un compte Microsoft Entra d'un employé.
*   **Cible de l'exfiltration :** Instance Salesforce de l'entreprise.
*   **Données compromises :** Noms, adresses e-mail, adresses physiques, numéros de téléphone et, pour une partie des employés, les intitulés de postes.
*   **Extorsion :** Les attaquants ont exigé une rançon pour supprimer les données ; face au refus de l'entreprise, ils ont publié les informations sur le dark web.
*   **Contexte :** ShinyHunters multiplie les attaques visant des instances Salesforce à travers le monde.

**Vulnérabilités :**
*   **Ingénierie sociale :** Succès d'une attaque par vishing contre un employé.
*   **Accès aux identités :** Compromission d'un compte privilégié (Microsoft Entra) permettant l'accès aux bases de données tierces (Salesforce).
*   *Note : Aucune CVE spécifique n'est associée à cet incident, l'attaque reposant sur l'exploitation humaine et la compromission d'identifiants.*

**Recommandations :**
*   **Renforcement de l'authentification :** Implémenter des méthodes d'authentification multifacteur (MFA) résistantes au phishing (clés matérielles FIDO2/WebAuthn).
*   **Formation des employés :** Sensibiliser le personnel aux techniques d'ingénierie sociale et de vishing.
*   **Sécurisation des accès SaaS :** Appliquer le principe du moindre privilège sur les instances tierces (type Salesforce) et surveiller étroitement les accès aux données volumineuses.
*   **Gestion des incidents :** Suivre les directives du FBI : ne jamais céder aux demandes de rançon, car cela ne garantit en rien la destruction des données volées.

---
[Source](https://www.bleepingcomputer.com/news/security/charter-communications-data-breach-affects-49-million-accounts/){:target="_blank"}
