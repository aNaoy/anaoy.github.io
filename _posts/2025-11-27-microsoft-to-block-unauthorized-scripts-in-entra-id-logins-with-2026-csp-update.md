---
title: 'Microsoft to Block Unauthorized Scripts in Entra ID Logins with 2026 CSP Update'
date: 2025-11-27
permalink: /posts/2025/11/27/microsoft-to-block-unauthorized-scripts-in-entra-id-logins-with-2026-csp-update/
tags:
- veille-cyber
- hackernews
---
**Sécurité Renforcée des Connexions Entra ID : Blocage des Scripts Non Autorisés**

Microsoft met en place une nouvelle mesure de sécurité pour renforcer la protection des connexions à Entra ID. À partir de mi-octobre 2026, l'entreprise bloquera l'exécution de scripts non autorisés lors du processus de connexion sur "login.microsoftonline.com". Cette mise à jour de la politique de sécurité du contenu (CSP) limitera l'exécution des scripts aux domaines de confiance de Microsoft, ajoutant une couche de défense contre les injections de code malveillant.

**Points Clés :**

*   **Objectif :** Prévenir les attaques par injection de scripts malveillants lors de l'authentification sur Entra ID.
*   **Mécanisme :** La mise à jour CSP autorisera uniquement les scripts provenant de domaines approuvés par Microsoft et l'exécution de scripts inline depuis une source de confiance.
*   **Portée :** La mesure s'applique spécifiquement aux expériences de connexion basées sur le navigateur pour les URL commençant par "login.microsoftonline.com". Les identités externes d'Entra ID ne seront pas affectées.
*   **Contexte :** Cette initiative s'inscrit dans le cadre de la "Secure Future Initiative" (SFI) de Microsoft, visant à prioriser la sécurité et à mieux se préparer aux menaces cybernétiques.

**Vulnérabilités concernées :**

Bien que l'article ne mentionne pas de CVE spécifiques pour cette future mise à jour, l'objectif est de prévenir les risques liés aux attaques de type :

*   **Cross-Site Scripting (XSS) :** Permettant l'injection de code malveillant dans les pages web.

**Recommandations :**

*   **Tests :** Les organisations sont invitées à tester minutieusement leurs flux de connexion avant la mise en œuvre pour garantir une expérience utilisateur fluide.
*   **Extensions de Navigateur :** Éviter l'utilisation d'extensions ou d'outils qui injectent du code ou des scripts dans le processus de connexion Microsoft Entra. Privilégier des alternatives qui n'impliquent pas d'injection de code.
*   **Identification des Violations CSP :** Pour détecter d'éventuelles violations, ouvrir la console de développement du navigateur lors d'un flux de connexion et rechercher les erreurs "Refused to load the script" liées aux directives "script-src" et "nonce".

---
[Source](https://thehackernews.com/2025/11/microsoft-to-block-unauthorized-scripts.html){:target="_blank"}
