---
title: '2025’s Top Phishing Trends and What They Mean for Your Security Strategy'
date: 2025-12-15
permalink: /posts/2025/12/15/2025s-top-phishing-trends-and-what-they-mean-for-your-security-strategy/
tags:
- veille-cyber
- bleepingcomp
---
## Évolution des Attaques par Phishing en 2025

En 2025, les cybercriminels ont fait preuve d'une grande innovation dans leurs méthodes de phishing, en se concentrant davantage sur l'usurpation d'identité. Cette évolution rend le phishing plus efficace que jamais.

### Tendances Clés Observées en 2025

*   **Phishing Omni-canal :** Les attaques ne se limitent plus à l'e-mail. Environ un tiers des attaques détectées ont eu lieu via d'autres canaux, tels que les messages directs sur LinkedIn et les publicités sur les moteurs de recherche (ex. Google Ads). Ces canaux contournent les protections traditionnelles de la messagerie et sont moins suspects pour les utilisateurs. Des campagnes ont ciblé des cadres d'entreprises technologiques avec de fausses opportunités d'investissement sur LinkedIn, et des publicités malveillantes ont été utilisées pour intercepter les recherches sur des termes clés.

*   **Domination des Kits de Phishing-as-a-Service (PhaaS) :** Ces kits, tels que Tycoon, NakedPages et diverses variantes d'Evilginx, permettent de contourner la plupart des authentifications multifacteurs (MFA) grâce à des attaques "Man-in-the-Middle" qui volent des sessions en temps réel. Ils rendent les techniques sophistiquées accessibles à un plus grand nombre de cybercriminels, abaissant ainsi le seuil d'entrée. Des techniques d'évasion de détection sont intégrées, notamment :
    *   L'utilisation de protections anti-bots (CAPTCHA, Cloudflare Turnstile) pour bloquer l'analyse par les outils de sécurité.
    *   Des chaînes de redirection complexes pour masquer les pages malveillantes.
    *   Le chargement conditionnel du contenu malveillant via JavaScript pour échapper à l'analyse du trafic réseau.

*   **Contournement des Méthodes d'Authentification Résistantes au Phishing :** Même les protections comme les passkeys ne sont pas infaillibles. Les attaquants développent des méthodes alternatives pour obtenir un accès :
    *   **Consent Phishing :** Inciter les victimes à autoriser des applications OAuth malveillantes.
    *   **Device Code Phishing :** Similaire au consent phishing, mais via le flux de code d'appareil.
    *   **Extensions de Navigateur Malveillantes :** Voler des identifiants et des cookies directement dans le navigateur.
    *   **ClickFix :** Technique où les utilisateurs sont incités à exécuter du code malveillant localement sous prétexte de "réparer" un problème web. Ce fut un vecteur d'accès initial majeur.
    *   **ConsentFix :** Une variante plus dangereuse de ClickFix, entièrement native au navigateur, qui établit des connexions OAuth via le simple copier-coller d'une URL contenant du matériel d'authentification sensible, ciblant notamment des applications critiques comme Azure CLI.

### Recommandations pour les Équipes de Sécurité en 2026

Les stratégies de sécurité doivent évoluer pour tenir compte de ces nouvelles menaces :

*   **Ne plus se limiter à la protection de la messagerie :** Les attaques se propagent désormais sur de multiples canaux.
*   **Reconnaître les limites des outils de surveillance réseau :** Ils peinent à suivre le rythme des pages de phishing modernes.
*   **Comprendre que même l'authentification résistante au phishing n'est pas une garantie absolue.**
*   **Mettre l'accent sur la détection et la réponse :** De nombreuses organisations souffrent de lacunes importantes en matière de visibilité.
*   **Combler le fossé de détection dans le navigateur :** Les attaques se déroulant dans le navigateur constituent une cible idéale pour la détection.

Des solutions basées sur la plateforme navigateur peuvent fournir des capacités complètes de détection et de réponse pour bloquer ces attaques, tout en permettant de découvrir et de corriger proactivement les vulnérabilités identitaires.

### Vulnérabilités

L'article ne mentionne pas de CVE spécifiques, mais décrit des types de vulnérabilités et de techniques exploitées :

*   **Contournement de MFA :** Exploité par les kits PhaaS et les attaques Man-in-the-Middle.
*   **Exploitation des flux d'authentification OAuth :** Via Consent Phishing et Device Code Phishing.
*   **Compromission du navigateur :** Via les extensions malveillantes, ClickFix et ConsentFix.
*   **Exploitation des vulnérabilités dans les applications natives (ex. Azure CLI) :** Permettant des accès non restreints.
*   **Faible visibilité sur les activités du navigateur :** Point aveugle pour la plupart des équipes de sécurité.

---
[Source](https://www.bleepingcomputer.com/news/security/2025s-top-phishing-trends-and-what-they-mean-for-your-security-strategy/){:target="_blank"}
