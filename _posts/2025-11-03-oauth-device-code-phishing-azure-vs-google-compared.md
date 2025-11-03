---
title: 'OAuth Device Code Phishing: Azure vs. Google Compared'
date: 2025-11-03
permalink: /posts/2025/11/03/oauth-device-code-phishing-azure-vs-google-compared/
tags:
- veille-cyber
- bleepingcomp
---
### Exploitation du Flux de Code Appareil OAuth : Différences entre Azure et Google

Le flux de code appareil (ou autorisation d'appareil) OAuth 2.0 est une méthode d'authentification conçue pour les appareils sans interface utilisateur complète, comme les objets connectés. Ce mécanisme permet à un utilisateur d'authentifier un tel appareil en utilisant un code numérique sur un appareil distinct doté d'un navigateur et d'un clavier.

Des chercheurs ont exploité ce flux pour mener des attaques de phishing. L'attaquant obtient un code appareil via une API légitime, puis incite la victime à l'entrer sur une page de connexion légitime (par exemple, microsoft.com/devicelogin), où elle saisit également ses identifiants et un code MFA. L'attaquant récupère ensuite les jetons d'accès générés.

**Points Clés :**

*   **Mécanisme du Flux de Code Appareil :** Permet l'authentification d'appareils à entrée limitée en utilisant un code à saisir sur un autre appareil.
*   **Attaque par Phishing de Code Appareil :** L'attaquant abuse de ce flux en trompant la victime pour qu'elle fournisse ses identifiants, obtenant ainsi des jetons d'accès.
*   **Attaque dans l'Écosystème Microsoft :** Dans Azure, cette attaque utilise des API et des URL légitimes de Microsoft, rendant la détection plus difficile. L'attaquant peut spécifier la ressource et un "Family of Client IDs" (IDs de client) publics, influençant la puissance du jeton obtenu.
*   **Impact Différent chez Google :** Google limite considérablement les permissions (scopes) autorisées pour le flux de code appareil, rendant l'exploitation beaucoup moins puissante.

**Vulnérabilités et Exploitation :**

*   **Attaque Générique :** Exploite le flux de code appareil OAuth 2.0, qui est une fonctionnalité standard. Aucun CVE spécifique n'est mentionné pour l'attaque elle-même, mais l'exploitation se base sur des fonctionnalités existantes.
*   **Azure :**
    *   **Vulnérabilité :** Absence de restrictions sur les permissions (scopes) et les ressources spécifiables lors de la génération du code appareil. Utilisation de "Family of Client IDs" publics qui permettent de débloquer des permissions étendues.
    *   **Exploitation :** Peut permettre d'obtenir des jetons très puissants, y compris des jetons d'actualisation primaires (Primary Refresh Tokens), permettant une prise de contrôle étendue (accès aux e-mails, calendrier, fichiers, inscription MFA, jonction de périphériques au tenant, etc.). L'attaquant contrôle la portée des jetons.
*   **Google :**
    *   **Vulnérabilité :** Implémentation du flux de code appareil qui restreint sévèrement les scopes disponibles (par exemple, accès limité aux fichiers Google Drive spécifiques à l'application ou lecture YouTube).
    *   **Exploitation :** Les jetons obtenus ont une portée très limitée, ne permettant généralement pas de prise de contrôle significative ou de pivotement vers d'autres ressources. L'obtention d'un ID client nécessite la création d'une application, contrairement à Azure où des IDs publics sont disponibles.

**Recommandations :**

*   **Pour Azure :**
    *   Surveiller les demandes d'accès via le flux de code appareil et les permissions demandées.
    *   Restreindre l'utilisation du flux de code appareil aux scénarios absolument nécessaires.
    *   Être particulièrement vigilant quant aux tentatives de phishing qui redirigent vers des pages de connexion légitimes comme `microsoft.com/devicelogin`.
    *   Comprendre le rôle et l'impact des "Family of Client IDs" et des ressources demandées lors de l'authentification.
    *   Examiner les permissions associées aux jetons obtenus et surveiller les activités suspectes qui en découlent.
*   **Pour Google :**
    *   Bien que l'implémentation soit plus restrictive, une surveillance des flux d'authentification reste pertinente.
    *   Être conscient que même avec des scopes limités, une compromission peut toujours avoir un impact si l'application légitime à laquelle le jeton est associé est critique.

En résumé, bien que le flux de code appareil soit une fonctionnalité standard OAuth 2.0, son implémentation par Microsoft et Google présente des différences majeures en termes de surface d'attaque, rendant cette technique de phishing beaucoup plus dangereuse dans l'écosystème Azure.

---
[Source](https://www.bleepingcomputer.com/news/security/oauth-device-code-phishing-azure-vs-google-compared/){:target="_blank"}
