---
title: 'Know Your Enemy: Browser-Based Attack Techniques in 2026'
date: 2026-09-30
permalink: /posts/2026/09/30/know-your-enemy-browser-based-attack-techniques-in-2026/
tags:
- veille-cyber
- hackernews
---
### État des menaces par navigateur en 2026 : Panorama et vecteurs d'attaque

Le navigateur web est devenu la plateforme principale des cyberattaques modernes, permettant d'exécuter des chaînes d'intrusion complètes, de l'accès initial à l'exfiltration de données, sans jamais quitter la session de navigation.

#### Points clés et techniques d'attaque
1.  **Phishing AiTM (Adversary-in-the-Middle) :** Utilisation de kits (Tycoon2FA, Evilginx) pour intercepter en temps réel les identifiants et les jetons de session, contournant ainsi la quasi-totalité des MFA.
2.  **ClickFix :** Vecteur d'accès dominant (52 % des détections). Il repose sur l'ingénierie sociale (fausses notifications CAPTCHA ou d'erreur) pour inciter l'utilisateur à copier-coller des commandes malveillantes dans son terminal.
3.  **Phishing par autorisation (OAuth) :** Abus des mécanismes OAuth (consentement, flux de code appareil) pour obtenir des jetons d'accès sans interagir avec le flux d'authentification habituel, rendant les clés de sécurité (passkeys) inopérantes.
4.  **Extensions malveillantes :** Détournement d'extensions légitimes via des mises à jour malveillantes. Plus de 46 % des extensions disposent de permissions permettant une prise de contrôle totale du compte.
5.  **Ghost Logins (Logins fantômes) :** Persistance de méthodes d'authentification locales (hors SSO) non protégées par MFA, souvent ignorées par les journaux d'identité des entreprises.
6.  **Vol de session :** Exfiltration de jetons de session via des infostealers, particulièrement sur des appareils non gérés ou via la synchronisation de profils de navigateur personnels sur des postes professionnels.

#### Vulnérabilités notables
*   **RFC 8628 :** Exploité via le phishing par code d'appareil pour contourner l'authentification standard.
*   *Note : Aucune CVE spécifique n'est mentionnée dans l'article, car ces attaques exploitent principalement le design légitime des protocoles (OAuth) et l'ingénierie sociale plutôt que des failles logicielles documentées.*

#### Recommandations de sécurité
*   **Approche « Default-Deny » pour les extensions :** Mettre en place une liste blanche (allowlist) et surveiller activement les changements de permissions plutôt que de se fier à des scores de risque statiques.
*   **Gestion des identités :** Identifier et désactiver les « ghost logins » et imposer le SSO sur l'ensemble des applications SaaS pour limiter l'usage de mots de passe faibles ou réutilisés.
*   **Renforcement hors périmètre :** Étendre la surveillance aux appareils non gérés (BYOD/contractants) et aux navigateurs où la synchronisation est active.
*   **Détection comportementale :** Privilégier des solutions de sécurité capables d'analyser les événements de navigation en temps réel (comme les événements de copier-coller suspects) plutôt que de se reposer uniquement sur des blocklists de domaines, souvent obsolètes en moins de 48 heures.

---
[Source](https://thehackernews.com/2026/09/know-your-enemy-browser-based-attack.html){:target="_blank"}
