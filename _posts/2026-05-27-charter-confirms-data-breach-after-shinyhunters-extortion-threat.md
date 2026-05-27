---
title: 'Charter confirms data breach after ShinyHunters extortion threat'
date: 2026-05-27
permalink: /posts/2026/05/27/charter-confirms-data-breach-after-shinyhunters-extortion-threat/
tags:
- veille-cyber
- bleepingcomp
---
### Cyberattaque contre Charter Communications par le groupe ShinyHunters

Le géant américain des télécommunications, Charter Communications, a confirmé avoir fait l'objet d'une tentative d'extorsion par le groupe de cybercriminels « ShinyHunters ». Les attaquants affirment avoir exfiltré les données de 40 millions de clients depuis la plateforme Salesforce de l'entreprise, bien que Charter assure qu'aucune donnée sensible ou information confidentielle réseau n'a été compromise.

**Points clés :**
*   **Mode opératoire :** L'intrusion initiale a été réalisée via une attaque par *vishing* (phishing vocal), permettant aux attaquants de compromettre un compte Microsoft Entra employé.
*   **Cible privilégiée :** Les attaquants exploitent les accès SSO (Single Sign-On) pour infiltrer des applications SaaS tierces comme Salesforce, Microsoft 365 ou Google Workspace.
*   **Méthode d'extorsion :** Le groupe menace de divulguer les bases de données volées si une rançon n'est pas versée, une stratégie appliquée récemment à d'autres organisations comme Instructure.

**Vulnérabilités :**
*   **Ingénierie sociale :** Sensibilité du personnel aux attaques par *vishing*.
*   **Gestion des accès :** Vulnérabilité des comptes SSO (Microsoft Entra) sans protection renforcée.
*   **Exfiltration SaaS :** Vol de jetons OAuth ou utilisation de comptes compromis pour exporter massivement des données depuis des plateformes CRM (Salesforce).
*   *Note : Aucune CVE spécifique n'est associée, l'attaque reposant sur l'exploitation de comptes légitimes.*

**Recommandations :**
*   **Renforcement de l'authentification :** Déployer une authentification multifacteur (MFA) résistante au phishing pour tous les accès SSO.
*   **Sensibilisation :** Former les employés à la détection des techniques de *vishing* et d'ingénierie sociale.
*   **Surveillance des accès SaaS :** Mettre en place des mécanismes de détection d'anomalies sur les exportations de données volumineuses depuis des instances Salesforce ou autres outils SaaS.
*   **Gestion des sessions :** Révoquer régulièrement les jetons OAuth et surveiller les connexions inhabituelles sur les comptes privilégiés.

---
[Source](https://www.bleepingcomputer.com/news/security/charter-confirms-data-breach-after-shinyhunters-extortion-threat/){:target="_blank"}
