---
title: 'Greatness PhaaS Adds Device Code Phishing to Bypass MFA and Steal Tokens'
date: 2026-08-04
permalink: /posts/2026/08/04/greatness-phaas-adds-device-code-phishing-to-bypass-mfa-and-steal-tokens/
tags:
- veille-cyber
- hackernews
---
### Évolution de la plateforme PhaaS "Greatness" : Menace par phishing via code d'appareil

La plateforme de phishing-as-a-service (PhaaS) **Greatness** a étendu ses capacités pour inclure le *device code phishing* (phishing par code d'appareil). Cet outil permet aux cybercriminels de contourner l'authentification multifacteur (MFA) en abusant des flux d'autorisation OAuth 2.0.

#### Points clés
*   **Expansion des capacités :** Greatness propose désormais, via une interface unique, le vol de jetons par intermédiaire (AiTM), l'abus de consentement OAuth et le phishing par code d'appareil.
*   **Méthodologie :** Les attaquants exploitent la confiance des utilisateurs en utilisant des leurres (ex: faux messages vocaux RingCentral) qui contournent les passerelles email grâce à des listes d'expéditeurs autorisés.
*   **Persistance :** Une fois les jetons volés, les attaquants utilisent l'API Microsoft Graph pour exfiltrer des données (Outlook, Teams, SharePoint) et enregistrent de nouveaux périphériques pour obtenir des jetons de rafraîchissement (PRT) garantissant un accès durable.
*   **Modèle économique :** La plateforme est disponible par abonnement (environ 289 $ par mois) via Telegram, incluant un tableau de bord complet et des modèles de phishing prêts à l'emploi.

#### Vulnérabilités exploitées
*   **Abus du flux d'autorisation OAuth 2.0 Device Code :** Permet d'obtenir des jetons d'accès sans que l'utilisateur n'ait à saisir ses identifiants sur une page frauduleuse, rendant l'attaque particulièrement difficile à détecter visuellement.
*   **Trust Configurations (Configuration de confiance) :** Exploitation des listes d'expéditeurs "Safe Sender" au sein des entreprises, souvent configurées suite à une fuite de données chez des prestataires tiers.

#### Recommandations
*   **Blocage des méthodes d'authentification :** Désactiver le flux "Device Code" au niveau global via les politiques d'accès conditionnel (*Conditional Access Policies*) si celui-ci n'est pas strictement nécessaire.
*   **MFA résistante au phishing :** Migrer vers des méthodes d'authentification forte résistantes au phishing (clés FIDO2/WebAuthn).
*   **Audit des listes blanches :** Réviser régulièrement les règles d'exclusion et les listes d'expéditeurs autorisés dans les passerelles de messagerie, particulièrement après la divulgation d'une violation de données chez un fournisseur tiers.
*   **Sensibilisation :** Éduquer les employés sur les risques liés aux codes de vérification inattendus demandés sur des appareils.

---
[Source](https://thehackernews.com/2026/08/greatness-phaas-adds-device-code.html){:target="_blank"}
