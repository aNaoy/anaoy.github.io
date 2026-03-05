---
title: 'Europol-Led Operation Takes Down Tycoon 2FA Phishing-as-a-Service Linked to 64,000 Attacks'
date: 2026-03-05
permalink: /posts/2026/03/05/europol-led-operation-takes-down-tycoon-2fa-phishing-as-a-service-linked-to-64000-attacks/
tags:
- veille-cyber
- hackernews
---
### Démantèlement de "Tycoon 2FA", un service de phishing à grande échelle

Une opération internationale menée par Europol a permis de démanteler "Tycoon 2FA", une plateforme de "phishing-as-a-service" (PhaaS) utilisée pour mener des attaques de type "adversary-in-the-middle" (AitM) à grande échelle. Ce service, apparu en août 2023, permettait aux cybercriminels de voler des identifiants et des codes d'authentification multifacteur (MFA).

**Points Clés:**

*   **Nature du service:** Tycoon 2FA était un kit de phishing par abonnement, vendu sur des plateformes de messagerie cryptée comme Telegram et Signal. Il proposait une interface d'administration pour configurer, suivre et affiner les campagnes de phishing.
*   **Mécanisme d'attaque:** Le service utilisait la technique AitM pour intercepter les identifiants, les codes MFA et les cookies de session, permettant ainsi aux attaquants d'obtenir un accès complet aux comptes compromis, même après une réinitialisation de mot de passe.
*   **Échelle des attaques:** Tycoon 2FA a été à l'origine de plus de 64 000 incidents de phishing, ciblant des dizaines de milliers d'organisations dans le monde, y compris des écoles, des hôpitaux et des institutions publiques. Microsoft a bloqué plus de 13 millions d'e-mails malveillants liés à ce service rien qu'en octobre 2025. Le service représentait environ 62% des tentatives de phishing bloquées par Microsoft à la mi-2025.
*   **Ciblage:** Les attaques visaient principalement les environnements professionnels, avec une forte concentration de victimes identifiées aux États-Unis, suivis du Royaume-Uni, du Canada, de l'Inde et de la France.
*   **Techniques d'évasion:** Le service utilisait des techniques sophistiquées comme la dissimulation de code, le suivi des frappes clavier, le filtrage des bots, l'empreinte digitale du navigateur, les CAPTCHA auto-hébergés, et l'utilisation de noms de domaine à courte durée de vie pour échapper à la détection.
*   **ATO Jumping:** Les utilisateurs de Tycoon 2FA exploitaient la technique "ATO Jumping", consistant à utiliser un compte compromis pour distribuer des liens de phishing Tycoon 2FA, augmentant ainsi la crédibilité des e-mails.

**Vulnérabilités exploitées:**

Bien que des CVE spécifiques ne soient pas mentionnés dans cet article, le principal vecteur de vulnérabilité réside dans la capacité de Tycoon 2FA à :

*   **Imiter les processus d'authentification légitimes:** Cela permet de tromper les utilisateurs et de subtiliser leurs identifiants et leurs codes MFA.
*   **Intercepter les cookies de session:** Permettant de maintenir la session d'un utilisateur même après la déconnexion ou la réinitialisation du mot de passe, tant que le cookie n'est pas révoqué.

**Recommandations (déduites de l'article):**

*   **Vigilance accrue face au phishing AitM:** Les utilisateurs doivent être particulièrement prudents face aux demandes d'authentification, surtout celles qui semblent inhabituelles ou proviennent de sources inattendues.
*   **Reconnaissance des tentatives de phishing:** Se méfier des e-mails ou des messages semblant provenir de marques de confiance, surtout s'ils demandent des informations sensibles.
*   **Mise à jour des systèmes de sécurité:** Les organisations doivent s'assurer que leurs solutions de sécurité email et de protection des terminaux sont à jour pour détecter et bloquer ce type d'attaques.
*   **Gestion rigoureuse des sessions et des cookies:** En cas de compromission suspectée, la révocation active des sessions et des cookies d'authentification est essentielle.
*   **Sensibilisation des employés:** Former régulièrement les utilisateurs aux risques du phishing et aux meilleures pratiques de cybersécurité est crucial.
*   **Surveillance des activités suspectes:** Mettre en place des systèmes de détection et de réponse aux incidents pour identifier rapidement les tentatives d'accès non autorisé.

---
[Source](https://thehackernews.com/2026/03/europol-led-operation-takes-down-tycoon.html){:target="_blank"}
