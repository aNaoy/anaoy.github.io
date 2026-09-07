---
title: 'Fake IT Calls Target Executives in Microsoft 365 Data Theft and Extortion Attacks'
date: 2026-09-07
permalink: /posts/2026/09/07/fake-it-calls-target-executives-in-microsoft-365-data-theft-and-extortion-attacks/
tags:
- veille-cyber
- hackernews
---
### Campagne d'extorsion et vol de données par « vishing » ciblant Microsoft 365

Le groupe de menace, suivi sous le nom **PREY-0058** (potentiellement lié à UNC6671/Pink/Cinder), mène une campagne sophistiquée de vol de données visant les cadres dirigeants. Cette attaque repose sur l'ingénierie sociale et des techniques de contournement d'authentification pour exfiltrer des informations sensibles sur des plateformes SaaS.

**Points clés :**
*   **Méthode d'attaque :** Utilisation du « vishing » (phishing vocal) où les attaquants se font passer pour le support informatique de l'entreprise.
*   **AitM (Adversary-in-the-Middle) :** Les victimes sont dirigées vers des sites frauduleux imitant les pages de connexion Microsoft 365 pour intercepter les identifiants et les jetons de session MFA.
*   **Infrastructure :** Utilisation de proxies résidentiels pour rejouer les sessions volées depuis des adresses IP géographiquement proches de la victime, rendant la détection plus complexe.
*   **Objectif :** Exfiltration massive de données via SharePoint, OneDrive, Exchange et Box, suivie d'une demande d'extorsion.
*   **Cibles :** Cadres supérieurs dans les secteurs de la construction, de la santé, de l'immobilier, de la finance et des services professionnels.

**Vulnérabilités :**
*   Il n'y a pas de vulnérabilité logicielle (CVE) spécifique exploitée. L'attaque exploite la vulnérabilité humaine et les faiblesses inhérentes aux méthodes d'authentification MFA basées sur des jetons de session (non résistantes au phishing).

**Recommandations :**
*   **Authentification :** Migrer vers des méthodes d'authentification multi-facteurs résistantes au phishing (clés FIDO2/WebAuthn).
*   **Accès conditionnel :** Configurer des politiques d'accès conditionnel strictes pour limiter les connexions suspectes provenant de proxies résidentiels.
*   **Surveillance :** Détecter les anomalies liées aux sessions (rejeu de jetons), aux recherches inhabituelles dans SharePoint et à l'accès massif à des fichiers.
*   **Sensibilisation :** Former le personnel (notamment les cadres et les équipes de support) aux risques de vishing et établir des protocoles de vérification d'identité pour les demandes informatiques sensibles.
*   **Moindre privilège :** Restreindre l'accès aux données sensibles dans SharePoint et OneDrive au strict nécessaire.

---
[Source](https://thehackernews.com/2026/09/microsoft-365-attackers-use-help-desk.html){:target="_blank"}
