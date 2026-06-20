---
title: 'Microsoft links Mastra AI supply chain attack to North Korean hackers'
date: 2026-06-20
permalink: /posts/2026/06/20/microsoft-links-mastra-ai-supply-chain-attack-to-north-korean-hackers/
tags:
- veille-cyber
- bleepingcomp
---
### Attaque de la chaîne d’approvisionnement npm : Le groupe Sapphire Sleet visé

Microsoft a attribué une attaque majeure sur la chaîne d'approvisionnement du framework Mastra au groupe de pirates nord-coréen Sapphire Sleet (également connu sous le nom de BlueNoroff). En compromettant le compte d'un mainteneur npm, les attaquants ont injecté du code malveillant dans plus de 140 paquets de l'écosystème Mastra.

**Points clés :**
*   **Vecteur d'attaque :** Compromission d'un compte de mainteneur npm (« ehindero ») pour publier des mises à jour corrompues.
*   **Méthode :** Injection d'une dépendance malveillante nommée `easy-day-js` (un *typosquat* de la bibliothèque légitime `dayjs`).
*   **Exécution :** Un script de post-installation (`postinstall hook`) désactive la vérification TLS et contacte un serveur de commande et contrôle (C2).
*   **Objectif :** Déploiement d'un logiciel malveillant multiplateforme (Windows, Linux, macOS) visant à exfiltrer des identifiants, des clés API et à dérober des portefeuilles de cryptomonnaies (166 extensions ciblées).
*   **Persistance :** Utilisation de méthodes spécifiques aux OS : clés de registre Windows, LaunchAgents macOS et services systemd sous Linux.

**Vulnérabilités :**
*   Aucune CVE spécifique n'est mentionnée, car l'attaque repose sur une compromission de compte légitime et une injection de code via une dépendance malveillante (*typosquatting*).

**Recommandations :**
*   **Auditer les dépendances :** Vérifier systématiquement les noms des paquets installés pour détecter les typosquattings (ex: `easy-day-js` au lieu de `dayjs`).
*   **Gestion des accès :** Imposer l'authentification multifacteur (MFA) sur tous les comptes disposant de droits de publication dans les registres de paquets.
*   **Surveillance réseau :** Surveiller les appels sortants suspects effectués par des processus de développement (scripts de post-installation) vers des serveurs inconnus.
*   **Sécurité des terminaux :** Utiliser des solutions EDR (Endpoint Detection and Response) pour bloquer les comportements anormaux, comme la désactivation des certificats TLS par des scripts ou l'installation de services non autorisés.

---
[Source](https://www.bleepingcomputer.com/news/security/microsoft-links-mastra-ai-supply-chain-attack-to-north-korean-hackers/){:target="_blank"}
