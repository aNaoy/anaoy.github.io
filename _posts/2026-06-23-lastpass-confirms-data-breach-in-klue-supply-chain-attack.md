---
title: 'LastPass confirms data breach in Klue supply chain attack'
date: 2026-06-23
permalink: /posts/2026/06/23/lastpass-confirms-data-breach-in-klue-supply-chain-attack/
tags:
- veille-cyber
- bleepingcomp
---
### Violation de données chez LastPass via l'attaque par chaîne d'approvisionnement Klue

LastPass a été victime d'une fuite de données au sein de son environnement Salesforce, suite au vol de jetons OAuth lors d'une attaque visant le fournisseur tiers Klue. Bien que les systèmes de gestion de mots de passe et les coffres-forts clients restent sécurisés, les données stockées dans l'environnement CRM ont été exposées. L'attaque, revendiquée par le groupe « Icarus », a exploité des identifiants hérités pour compromettre l'infrastructure de Klue et accéder aux jetons d'intégration.

**Points clés :**
*   **Vecteur d'attaque :** Utilisation de jetons OAuth dérobés à Klue pour accéder aux données Salesforce de LastPass.
*   **Données exposées :** Noms, numéros de téléphone, adresses e-mail, adresses physiques, informations de support technique et données CRM.
*   **Impact :** Aucun accès aux coffres-forts des utilisateurs ni aux données de la plateforme Gong. Plusieurs autres organisations ont été touchées par cette campagne d'extorsion.

**Vulnérabilités :**
*   **Compromission d'identifiants hérités :** Utilisation de comptes obsolètes pour accéder à l'infrastructure de Klue.
*   **CVE :** Aucune CVE spécifique n'est associée à cet incident, celui-ci reposant sur une exploitation de privilèges via des jetons d'authentification (OAuth).

**Recommandations :**
*   **Vigilance accrue :** Soyez extrêmement prudent face aux communications non sollicitées (e-mails ou appels) utilisant des domaines suspects comme `baccarat.com.au` ou `robinskitchen.com.au`.
*   **Protection des accès :** Ne partagez jamais votre mot de passe maître, même en cas de demande provenant d'un support technique présumé.
*   **Sécurité proactive :** LastPass a déjà révoqué les jetons API/OAuth exposés et coupé l'accès à Klue. Il est conseillé aux utilisateurs de surveiller leurs comptes pour détecter toute tentative de phishing ou d'ingénierie sociale exploitant les données volées.

---
[Source](https://www.bleepingcomputer.com/news/security/lastpass-confirms-data-breach-in-klue-supply-chain-attack/){:target="_blank"}
