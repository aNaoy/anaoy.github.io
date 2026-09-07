---
title: 'BigBear Microsoft 365 phishing service bypassed MFA at 258 organizations'
date: 2026-09-07
permalink: /posts/2026/09/07/bigbear-microsoft-365-phishing-service-bypassed-mfa-at-258-organizations/
tags:
- veille-cyber
- bleepingcomp
---
### Menace Phishing BigBear 2.0 : Contournement du MFA et compromission de Microsoft 365

Le framework de "Phishing-as-a-Service" (Phaas) **BigBear 2.0** a permis de compromettre 258 organisations et de dérober plus de 5 000 identifiants Microsoft 365. Cette campagne utilise une architecture de type Adversary-in-the-Middle (AiTM) pour intercepter les sessions authentifiées, rendant inefficace le MFA classique.

**Points clés :**
*   **Mode opératoire :** Utilisation du framework Evilginx2 pour créer des proxys transparents entre la victime et les serveurs Microsoft.
*   **Volume de données :** Plus de 5 100 enregistrements dérobés, incluant 474 sessions avec MFA contourné et 4 148 cookies de session.
*   **Techniques avancées :** 
    *   Utilisation de proxys résidentiels géolocalisés pour éviter les détections de connexion suspecte.
    *   Injection de scripts JavaScript personnalisés pour désactiver les protocoles FIDO2/WebAuthn côté navigateur, forçant l'utilisateur vers des méthodes MFA plus faibles.
*   **Infrastructure :** Un panel d'administration centralisé contrôlant 42 serveurs privés virtuels (VPS) et loué à plusieurs affiliés.

**Vulnérabilités :**
*   L'attaque exploite la capacité à intercepter et rejouer des jetons de session (AiTM).
*   *Note : Aucune CVE spécifique n'est associée à cette campagne, celle-ci reposant sur une manipulation logique des flux d'authentification et non sur une faille logicielle de Microsoft.*

**Recommandations :**
*   **Renforcement de l'authentification :** Imposer l'utilisation de clés de sécurité FIDO2/WebAuthn, lesquelles sont intrinsèquement résistantes au phishing AiTM.
*   **Gestion des accès :** Appliquer des politiques d'accès conditionnel exigeant des appareils gérés par l'entreprise plutôt que de se baser uniquement sur la géolocalisation.
*   **Remédiation immédiate :** En cas de compromission suspectée, réinitialiser les mots de passe, révoquer toutes les sessions actives et forcer une ré-authentification pour les comptes à hauts privilèges.

---
[Source](https://www.bleepingcomputer.com/news/security/bigbear-microsoft-365-phishing-service-bypassed-mfa-at-258-organizations/){:target="_blank"}
