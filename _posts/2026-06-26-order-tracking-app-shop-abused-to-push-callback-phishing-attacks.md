---
title: 'Order-tracking app Shop abused to push callback phishing attacks'
date: 2026-06-26
permalink: /posts/2026/06/26/order-tracking-app-shop-abused-to-push-callback-phishing-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Détournement de l'application Shop pour des campagnes de phishing par rappel

L'application de suivi de commandes « Shop » (Shopify) est actuellement exploitée par des cybercriminels pour mener des attaques de type *callback phishing*. Les attaquants injectent de faux reçus d'achat dans l'historique des utilisateurs, imitant des marques reconnues (Norton, McAfee, Apple, PayPal) afin d'inciter les victimes à contacter un prétendu service client.

**Points clés :**
*   **Méthodologie :** Les escrocs insèrent de fausses factures dans l'application, exploitant la confiance des utilisateurs envers cette plateforme légitime.
*   **Objectif :** Obtenir des identifiants de compte, des informations bancaires, des codes d'authentification (OTP) ou inciter l'installation de logiciels d'accès à distance.
*   **Vecteur d'injection :** Le mécanisme exact d'injection des faux reçus dans l'application reste indéterminé, bien que l'application puisse parser des e-mails ou se lier à des comptes tiers. Aucune compromission de l'infrastructure de Shopify n'a été détectée.

**Vulnérabilités :**
*   Aucune CVE spécifique n'est associée, car il s'agit d'un abus de fonctionnalités légitimes (*social engineering*) plutôt que d'une faille logicielle directe.

**Recommandations :**
*   **Vigilance :** Ne jamais appeler les numéros de téléphone indiqués sur des factures suspectes trouvées dans l'application.
*   **Signalement :** Utiliser la fonction de signalement intégrée à l'application Shop pour rapporter les boutiques frauduleuses.
*   **Vérification :** En cas de doute, contacter directement sa banque ou le service client officiel de la marque concernée via ses canaux habituels.
*   **Réaction en cas de compromission :** Si des données sensibles ont été transmises, réinitialiser immédiatement les mots de passe et contacter l'émetteur de la carte bancaire pour une opposition ou une surveillance renforcée.

---
[Source](https://www.bleepingcomputer.com/news/security/order-tracking-app-shop-abused-to-push-callback-phishing-attacks/){:target="_blank"}
