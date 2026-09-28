---
title: 'US soldier gets 70 months in prison for extorting 10 tech, telecom firms'
date: 2026-09-28
permalink: /posts/2026/09/28/us-soldier-gets-70-months-in-prison-for-extorting-10-tech-telecom-firms/
tags:
- veille-cyber
- bleepingcomp
---
### Condamnation d'un soldat américain pour cyber-extorsion

Cameron John Wagenius, un ancien soldat de l'armée américaine de 21 ans, a été condamné à 70 mois de prison et au paiement de près de 300 000 $ de dédommagement pour le piratage et l'extorsion de dix entreprises technologiques et de télécommunications. Entre avril 2023 et décembre 2024, il a utilisé des outils de force brute SSH pour voler des identifiants, revendre des données sensibles et pratiquer le *SIM-swapping*.

**Points clés :**
* **Mode opératoire :** Utilisation d'un outil de force brute SSH développé par l'auteur, coordination via Telegram et extorsion des entreprises sous la menace de publier les données volées sur des forums spécialisés (BreachForums, XSS.is).
* **Envergure :** Wagenius a tenté d'extorquer au moins 1 million de dollars à ses victimes.
* **Connexions :** Ses complices sont liés à la vaste campagne de piratage ayant visé la plateforme Snowflake, impactant plus de 165 organisations (dont AT&T, Ticketmaster, Santander) et des centaines de millions de clients.

**Vulnérabilités exploitées :**
* **Attaques par force brute :** Utilisation de scripts automatisés pour compromettre les accès SSH (souvent facilités par des mots de passe faibles).
* **Défaut d'authentification forte :** Les accès aux comptes clients et aux environnements cloud (Snowflake) ont été facilités par l'absence d'authentification multi-facteurs (MFA).

**Recommandations :**
* **Renforcement des accès :** Imposer l'authentification multi-facteurs (MFA) sur tous les comptes et accès distants.
* **Politique de mots de passe :** Exiger des mots de passe robustes (minimum 14 caractères).
* **Sécurisation SSH :** Désactiver l'authentification par mot de passe pour le SSH au profit des clés cryptographiques et restreindre les tentatives de connexion par une limitation de débit (rate limiting) ou un blocage IP après échecs répétés.

---
[Source](https://www.bleepingcomputer.com/news/security/us-soldier-gets-70-months-in-prison-for-extorting-10-tech-telecom-firms/){:target="_blank"}
