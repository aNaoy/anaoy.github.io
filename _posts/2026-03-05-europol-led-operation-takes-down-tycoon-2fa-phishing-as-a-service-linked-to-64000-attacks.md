---
title: 'Europol-Led Operation Takes Down Tycoon 2FA Phishing-as-a-Service Linked to 64,000 Attacks'
date: 2026-03-05
permalink: /posts/2026/03/05/europol-led-operation-takes-down-tycoon-2fa-phishing-as-a-service-linked-to-64000-attacks/
tags:
- veille-cyber
- hackernews
---
## Démantèlement d'une Plateforme de Phishing à Grande Échelle

Une opération internationale menée par Europol a permis de démanteler "Tycoon 2FA", un service de phishing-as-a-service (PhaaS) qui facilitait les attaques par émulation de l'attaquant au milieu (AitM) à grande échelle. Ce service, actif depuis août 2023, permettait à des cybercriminels d'obtenir des identifiants et des codes d'authentification multifacteur (MFA).

**Points Clés :**

*   **Vaste Portée :** Tycoon 2FA a été à l'origine de plus de 64 000 incidents de phishing et a ciblé près de 100 000 organisations mondialement, incluant des écoles, des hôpitaux et des institutions publiques. Environ 96 000 victimes distinctes ont été identifiées depuis 2023.
*   **Modèle Économique :** Le service était proposé sous forme d'abonnement via des plateformes de messagerie cryptée, avec des tarifs débutant à 120 USD pour 10 jours.
*   **Fonctionnalités Avancées :** La plateforme comprenait un panneau d'administration web pour configurer, suivre et affiner les campagnes de phishing. Elle offrait des modèles, des fichiers de leurre, des configurations de domaines et d'hébergement, ainsi qu'un système de suivi des victimes et des tentatives de connexion.
*   **Capture d'Informations :** Les données récoltées, comme les identifiants, les codes MFA et les cookies de session, pouvaient être téléchargées directement ou transmises via Telegram pour un suivi quasi en temps réel.
*   **Techniques d'Évasion :** Tycoon 2FA utilisait des techniques de contournement telles que la surveillance des frappes clavier, le filtrage anti-bots, le navigateur fingerprinting, l'obfuscation de code poussée, des CAPTCHA auto-hébergés, du JavaScript personnalisé et des pages de diversion dynamiques. L'utilisation de domaines à courte durée de vie sur des infrastructures comme Cloudflare complexifiait la détection.
*   **"ATO Jumping" :** Les clients de Tycoon 2FA utilisaient la technique de "ATO Jumping" (Account Takeover Jumping) en exploitant des comptes compromis pour distribuer des liens de phishing et mener d'autres tentatives de prise de contrôle.
*   **Ciblage Principal :** L'analyse a révélé que les comptes ciblés étaient majoritairement d'entreprise ou associés à des domaines payants, indiquant une orientation vers les environnements professionnels.
*   **Opération de Démantèlement :** Une coalition d'agences de maintien de l'ordre et d'entreprises de sécurité a saisi 330 domaines liés au service. Le principal développeur, Saad Fridi, basé au Pakistan, a été identifié.

**Vulnérabilités Exploités :**

*   **Compromission d'Identifiants et de Codes MFA :** La capacité du service à intercepter les identifiants et les codes MFA permettait des prises de contrôle de compte complètes, même lorsque l'authentification multifacteur était activée. L'interception des cookies de session permettait de maintenir l'accès même après une réinitialisation de mot de passe si les sessions actives n'étaient pas révoquées.

**Recommandations :**

Bien que l'article se concentre sur le démantèlement du service, les informations qu'il contient impliquent plusieurs recommandations générales pour la sécurité :

*   **Vigilance Accrue :** Être particulièrement prudent face aux tentatives de phishing, surtout celles qui imitent des marques de confiance ou proviennent de contacts apparemment légitimes.
*   **Revocation des Sessions :** En cas de suspicion de compromission, révoquer activement toutes les sessions actives et les jetons d'authentification des services concernés.
*   **Solutions de Sécurité d'Email :** Utiliser des solutions de sécurité d'email robustes capables de détecter et de bloquer les emails de phishing sophistiqués.
*   **Sensibilisation des Employés :** Renforcer la formation et la sensibilisation des employés aux risques du phishing et aux bonnes pratiques de sécurité.
*   **Surveillance des Comptes :** Mettre en place une surveillance active des comptes pour détecter toute activité suspecte ou non autorisée.

---
[Source](https://thehackernews.com/2026/03/europol-led-operation-takes-down-tycoon.html){:target="_blank"}
