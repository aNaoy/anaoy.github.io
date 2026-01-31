---
title: 'Mandiant Finds ShinyHunters-Style Vishing Attacks Stealing MFA to Breach SaaS Platforms'
date: 2026-01-31
permalink: /posts/2026/01/31/mandiant-finds-shinyhunters-style-vishing-attacks-stealing-mfa-to-breach-saas-platforms/
tags:
- veille-cyber
- hackernews
---
### Expansion des attaques de vishing ciblant les plateformes SaaS

Des groupes de cybercriminels, utilisant des tactiques similaires à celles du groupe ShinyHunters, étendent leurs activités d'extorsion en ciblant les plateformes SaaS (Software as a Service). Ces attaques exploitent des techniques d'ingénierie sociale avancées, notamment le vishing (hameçonnage vocal) et de faux sites de collecte d'identifiants, pour dérober les informations de connexion (SSO) et les codes d'authentification multifacteur (MFA). L'objectif final est de s'emparer de données sensibles et de communications internes, puis d'extorquer les victimes.

Mandiant suit ces activités sous plusieurs clusters, dont UNC6661, UNC6671 et UNC6240 (ShinyHunters), pour tenir compte de l'évolution des méthodes. Les acteurs de la menace continuent d'élargir le spectre des plateformes cloud visées et d'intensifier leurs tactiques d'extorsion, incluant le harcèlement du personnel des entreprises victimes.

**Points Clés :**

*   **Technique principale :** Vishing et faux sites web pour voler identifiants SSO et codes MFA.
*   **Cible :** Plateformes SaaS pour s'emparer de données sensibles et pratiquer l'extorsion.
*   **Groupes associés :** ShinyHunters (UNC6240), UNC6661, UNC6671.
*   **Escalade des tactiques :** Harcèlement des victimes, envoi de courriels de phishing à partir de comptes compromis, suppression de traces.
*   **Accès à des plateformes spécifiques :** Notamment des comptes clients Okta, et exfiltration de données depuis SharePoint et OneDrive via PowerShell.
*   **Absence de vulnérabilité logicielle :** Les attaques reposent sur l'efficacité de l'ingénierie sociale.

**Vulnérabilités et Vecteurs d'Attaque :**

*   **Hameçonnage vocal (Vishing) :** Les attaquants se font passer pour le personnel informatique afin d'inciter les employés à mettre à jour leurs informations de MFA sur des sites frauduleux.
*   **Collecte d'identifiants et de codes MFA :** Les informations dérobées permettent aux attaquants de s'enregistrer pour le MFA sur leur propre appareil et d'accéder aux environnements des victimes.
*   **Abus de plateformes cloud :** Utilisation d'identifiants compromis pour accéder et exfiltrer des données de services comme SharePoint et OneDrive.

**Recommandations :**

*   **Renforcement des processus d'assistance :** Exiger des appels vidéo en direct pour vérifier l'identité du personnel lors des requêtes.
*   **Limitation des accès :** Restreindre l'accès aux points de sortie fiables et aux emplacements physiques.
*   **Sécurisation des authentifications :**
    *   Mettre en place des mots de passe robustes.
    *   Supprimer l'utilisation du SMS, des appels téléphoniques et des e-mails comme méthodes d'authentification.
    *   Privilégier des méthodes d'authentification résistantes au phishing, comme les clés de sécurité FIDO2 ou les passkeys.
*   **Contrôle du plan de gestion :** Restreindre l'accès, auditer les secrets exposés et appliquer des contrôles d'accès aux appareils.
*   **Mise en place de la journalisation :** Améliorer la visibilité sur les actions d'identité, les autorisations et les comportements d'exportation de données SaaS.
*   **Détection des modifications MFA :** Surveiller l'enregistrement des appareils MFA et les changements de cycle de vie.
*   **Surveillance des événements d'autorisation :** Détecter les événements OAuth ou d'autorisation d'application suspects, ainsi que les activités d'identité en dehors des heures normales de bureau.

---
[Source](https://thehackernews.com/2026/01/mandiant-finds-shinyhunters-using.html){:target="_blank"}
