---
title: 'Forg365 PhaaS Targets Microsoft 365 with Device Code and AitM Session Theft'
date: 2026-07-13
permalink: /posts/2026/07/13/forg365-phaas-targets-microsoft-365-with-device-code-and-aitm-session-theft/
tags:
- veille-cyber
- hackernews
---
### Forg365 : Une menace PhaaS sophistiquée ciblant Microsoft 365

Forg365 est une nouvelle plateforme de « Phishing-as-a-Service » (PhaaS) vendue sur Telegram (400 $/mois) qui automatise le vol de comptes Microsoft 365. Elle combine des techniques de phishing par code d'appareil (*device code phishing*), des attaques par intermédiaire (*Adversary-in-the-Middle* ou AitM) et l'utilisation de l'IA pour générer des messages convaincants.

**Points clés :**
*   **Infrastructure légitime :** Le kit utilise des services comme Amazon SES et Twilio SendGrid pour envoyer des emails de phishing, permettant de contourner les filtres de sécurité traditionnels.
*   **Contournement de la sécurité :** La plateforme détecte les VPN et les scanners automatisés pour masquer son contenu malveillant derrière des pages légitimes (leurres) si l'accès est jugé suspect.
*   **Persistance post-compromission :** Une extension de navigateur dédiée, « ForgCookie », permet aux attaquants de maintenir l'accès au compte en actualisant automatiquement les cookies de session et les jetons OAuth, même après une déconnexion.
*   **Automatisation poussée :** Le tableau de bord permet de surveiller les boîtes mail compromises et d'utiliser l'IA pour répondre automatiquement à des fils de discussion existants afin de propager l'attaque.

**Vulnérabilités exploitées :**
Il n'existe pas de CVE spécifique, car l'attaque repose sur l'abus de fonctionnalités légitimes de Microsoft :
*   **Flux d'authentification par code d'appareil (Device Code Flow) :** Permet aux attaquants de générer des codes qui, une fois validés par la victime, autorisent une session contrôlée par l'attaquant.
*   **Tokens OAuth :** Vol et injection de jetons de rafraîchissement pour conserver l'accès au compte sans avoir besoin de mot de passe ou de second facteur.

**Recommandations :**
*   **Désactivation du flux de code d'appareil :** Bloquer cette méthode d'authentification dans les paramètres Microsoft 365 si elle n'est pas strictement nécessaire pour les besoins métier.
*   **Audit des accès :** Surveiller régulièrement les logs de connexion à la recherche d'activités inhabituelles suite à l'utilisation de codes d'appareil.
*   **Nettoyage des identités :** Supprimer les alias de messagerie obsolètes (legacy aliases) et les redirections d'emails provenant d'anciennes infrastructures, souvent utilisés comme vecteurs d'entrée.
*   **Gestion des règles de flux de courrier :** Auditer les règles de transport et de transfert automatique pour détecter des configurations anormales mises en place par des attaquants.

---
[Source](https://thehackernews.com/2026/07/forg365-phaas-targets-microsoft-365.html){:target="_blank"}
