---
title: 'Hedge fund cyberattacks tied to BlackFile-linked UNC6671 extortion group'
date: 2026-08-07
permalink: /posts/2026/08/07/hedge-fund-cyberattacks-tied-to-blackfile-linked-unc6671-extortion-group/
tags:
- veille-cyber
- bleepingcomp
---
### Vague d'attaques par vishing contre le secteur financier par le groupe UNC6671

Le groupe d'extorsion UNC6671 (associé à la marque BlackFile, récemment rebaptisée Redact) mène une campagne sophistiquée ciblant des fonds spéculatifs, des sociétés de capital-investissement et des institutions financières majeures. Ces cyberattaques exploitent l'ingénierie sociale pour infiltrer les environnements cloud des entreprises.

**Points clés :**
*   **Mode opératoire :** Utilisation du *vishing* (phishing vocal) où les attaquants se font passer pour le service informatique (helpdesk) de l'entreprise.
*   **Technique d'attaque :** Les victimes sont incitées à se connecter sur des sites frauduleux imitant les portails internes, permettant aux attaquants d'utiliser des kits *Adversary-in-the-Middle* (AitM) pour dérober des identifiants et des jetons de session en temps réel.
*   **Impact :** Une fois le SSO (Microsoft 365 ou Okta) compromis, les attaquants accèdent aux plateformes cloud, extraient des données sensibles et suppriment les preuves de connexion (e-mails de réinitialisation, notifications de sécurité).
*   **Mise en cause :** Les autorités de renseignement de Google (GTIG) attribuent ces actions à un noyau unique d'attaquants utilisant diverses marques (Redact, Pink, Helix, Falcon) pour masquer leurs activités.

**Vulnérabilités :**
*   L'attaque ne repose pas sur des CVE spécifiques mais sur des failles humaines et la confiance accordée au processus d'authentification multifacteur (MFA). La compromission des jetons de session (session cookies) contourne les protections MFA classiques.

**Recommandations :**
*   **Sensibilisation :** Former les employés à la vigilance concernant les appels téléphoniques non sollicités prétendant provenir du support informatique, surtout lorsqu'ils demandent une action immédiate sur les paramètres MFA.
*   **Sécurité des accès :** Mettre en œuvre des mécanismes d'authentification résistants au phishing (comme les clés de sécurité matérielles FIDO2/WebAuthn).
*   **Surveillance :** Renforcer la surveillance des journaux de connexion SSO pour détecter des accès inhabituels et mettre en place des alertes sur la modification des paramètres de sécurité ou la suppression de messages dans les boîtes de réception.
*   **Réponse aux incidents :** Automatiser la détection des comportements anormaux au sein des environnements cloud pour limiter l'exfiltration de données après une compromission initiale.

---
[Source](https://www.bleepingcomputer.com/news/security/hedge-fund-cyberattacks-tied-to-blackfile-linked-unc6671-extortion-group/){:target="_blank"}
