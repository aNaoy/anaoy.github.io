---
title: 'Microsoft 365 AitM Phishing Hijacks Accounts to Collect Payroll and Finance Emails'
date: 2026-08-07
permalink: /posts/2026/08/07/microsoft-365-aitm-phishing-hijacks-accounts-to-collect-payroll-and-finance-emails/
tags:
- veille-cyber
- hackernews
---
### Campagne de phishing AitM : Menace sur les processus financiers de Microsoft 365

Une vaste campagne de phishing de type *Adversary-in-the-Middle* (AitM) cible les comptes Microsoft 365 pour s'introduire dans les processus de paie et de finance des entreprises. Attribuée au groupe « Payroll Pirates » (notamment Storm-2755), cette attaque utilise des techniques sophistiquées pour contourner les protections standards.

**Points clés :**
*   **Technique AitM :** Les attaquants créent des pages de connexion factices qui agissent comme un proxy, capturant en temps réel les identifiants et les codes d'authentification multifacteur (MFA).
*   **Infrastructure de redirection :** Utilisation de services légitimes (Google Meet, Google Ads, AWS S3) pour éviter les filtres de réputation.
*   **Contournement géographique :** Utilisation de proxies résidentiels situés dans le pays de la victime pour simuler un trafic local et éviter les alertes de connexion inhabituelle.
*   **Ciblage discret :** Les attaquants ciblent les ressources humaines et les services financiers pour détourner des paiements ou voler des informations confidentielles, tout en limitant leurs actions (peu de modifications de compte) pour éviter d'être détectés.
*   **Persistance :** Maintien des sessions compromises par des accès automatisés toutes les huit heures.

**Vulnérabilités :**
*   Cette attaque ne repose pas sur une vulnérabilité logicielle spécifique (CVE), mais sur l'exploitation des mécanismes d'authentification OAuth et la capacité à intercepter les jetons de session via des pages de phishing avancées.

**Recommandations :**
*   **Authentification résistante au phishing :** Migrer vers des méthodes MFA basées sur FIDO2/WebAuthn (clés de sécurité physiques), qui protègent contre les attaques AitM.
*   **Surveillance des accès :** Détecter les anomalies dans les agents utilisateurs (User-Agents) et les combinaisons navigateur/OS incohérentes (ex: mobile Safari sur Windows).
*   **Analyse comportementale :** Surveiller les accès via des proxies résidentiels et les connexions récurrentes (toutes les ~8h) provenant d'adresses IP rotatives conservant le même *SessionID*.
*   **Politiques d'accès conditionnel :** Restreindre les accès aux applications critiques en fonction de la conformité des appareils et des localisations géographiques strictes.

---
[Source](https://thehackernews.com/2026/08/microsoft-365-aitm-phishing-hijacks.html){:target="_blank"}
