---
title: 'Microsoft: Canadian employees targeted in payroll pirate attacks'
date: 2026-04-10
permalink: /posts/2026/04/10/microsoft-canadian-employees-targeted-in-payroll-pirate-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Attaques par "piratage de paie" contre les employés canadiens

Le groupe cybercriminel Storm-2755 mène actuellement des campagnes de "piratage de paie" visant à détourner les salaires d'employés canadiens. En utilisant des techniques de référencement malveillant (SEO poisoning) et de publicité trompeuse (malvertising), les attaquants redirigent les victimes vers de fausses pages de connexion Microsoft 365 pour dérober leurs jetons de session.

**Points clés :**
*   **Technique AiTM (Adversary-in-the-Middle) :** Les attaquants capturent les cookies de session et les jetons OAuth en temps réel, permettant de contourner les protections MFA (authentification multifacteur) classiques.
*   **Détournement de fonds :** Une fois l'accès obtenu, les attaquants masquent les communications avec les ressources humaines via des règles de boîte de réception, puis tentent de modifier les coordonnées bancaires des employés pour intercepter les virements de salaire.
*   **Accès direct :** Si l'ingénierie sociale échoue, ils accèdent directement aux plateformes RH (ex: Workday) pour effectuer les modifications manuellement.

**Vulnérabilités :**
*   L'article ne mentionne pas de CVE spécifique, mais souligne la vulnérabilité intrinsèque des **systèmes MFA hérités (non résistants au hameçonnage)** face aux attaques par interception de jetons (AiTM).

**Recommandations :**
*   **Renforcer l'authentification :** Migrer vers une MFA résistante au hameçonnage (norme FIDO2/WebAuthn).
*   **Bloquer l'authentification héritée :** Désactiver les protocoles d'authentification obsolètes.
*   **Réponse aux incidents :** En cas de compromission, révoquer immédiatement les jetons et sessions actifs, supprimer les règles de boîte de réception suspectes et réinitialiser les identifiants et méthodes MFA des comptes touchés.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-canadian-employees-targeted-in-payroll-pirate-attacks/){:target="_blank"}
