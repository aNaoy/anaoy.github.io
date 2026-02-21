---
title: 'Japanese-Language Phishing Emails, (Sat, Feb 21st)'
date: 2026-02-21
permalink: /posts/2026/02/21/japanese-language-phishing-emails-sat-feb-21st/
tags:
- veille-cyber
- sans-isc
---
**Campagne de Phishing Ciblée en Langue Japonaise**

Une campagne de phishing en langue japonaise utilise des emails frauduleux se faisant passer pour des entreprises connues telles que la compagnie aérienne ANA, la société de logistique DHL, et la compagnie de services publics myTOKYOGAS. Ces emails visent à tromper les destinataires pour obtenir des informations sensibles.

**Points Clés :**

*   **Langue :** Les emails sont rédigés en japonais.
*   **Impersonation :** Se font passer pour des entreprises légitimes (ANA, DHL, myTOKYOGAS).
*   **Structure :** Malgré les thèmes variés, les emails partagent un schéma similaire dans les URL des pages de phishing et les adresses d'envoi.
*   **Indicateurs Techniques :**
    *   Les domaines des adresses d'envoi et des liens de phishing utilisent le domaine de premier niveau (.cn).
    *   L'en-tête "X-mailer: Foxmail 6, 13, 102, 15 [cn]" est un indicateur fort que ces emails proviennent du même groupe.
    *   Les adresses IP d'envoi identifiées incluent 150.5.129.136, 101.47.78.193 et 150.5.130.42.

**Vulnérabilités Exploités :**

Bien qu'aucun CVE spécifique ne soit mentionné dans l'article, le vecteur d'attaque repose sur :

*   La **confiance** que les utilisateurs accordent aux emails apparemment légitimes.
*   L'**ingénierie sociale** pour inciter les utilisateurs à cliquer sur des liens malveillants ou à fournir des informations.
*   La potentielle **déficience des filtres anti-spam** chez certains utilisateurs, permettant à ces emails d'atteindre leur boîte de réception.

**Recommandations :**

*   **Vigilance accrue :** Être très prudent avec les emails non sollicités, surtout ceux demandant des informations personnelles ou financières.
*   **Vérification des expéditeurs :** Examiner attentivement l'adresse de l'expéditeur et ne pas se fier uniquement au nom affiché.
*   **Analyse des liens :** Survoler les liens sans cliquer pour vérifier leur destination réelle. Méfier des URL suspectes ou raccourcies.
*   **Filtrage anti-spam :** S'assurer que les filtres anti-spam sont activés et configurés de manière optimale.
*   **Sensibilisation :** Informer les utilisateurs sur les techniques de phishing courantes et les risques associés.
*   **Signalement :** Signaler les emails suspects aux fournisseurs de messagerie ou aux services de sécurité.

---
[Source](https://isc.sans.edu/diary/rss/32734){:target="_blank"}
