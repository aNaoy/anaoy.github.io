---
title: 'Most Wanted: The Phishing Kits and Techniques Getting Past Security Controls'
date: 2026-11-26
permalink: /posts/2026/11/26/most-wanted-the-phishing-kits-and-techniques-getting-past-security-controls/
tags:
- veille-cyber
- hackernews
---
### L'évolution des kits de phishing : La menace du "DOM Mirroring"

L'efficacité des attaques de phishing ne se mesure plus par le nombre de tentatives, mais par le **taux de percée** (*breakthrough rate*), c'est-à-dire la capacité d'un kit à contourner les passerelles de sécurité (email, web, filtrage) pour atteindre directement le navigateur de la victime.

**Points clés :**
*   **Contournement des défenses :** Les attaques modernes évitent souvent le courrier électronique au profit de vecteurs plus "crédibles" (invitations calendrier, publicités de recherche, QR codes).
*   **Technique du "DOM Mirroring" :** Il s'agit de la méthode d'interception (AiTM - *Adversary-in-the-Middle*) la plus récente et croissante. Contrairement aux pages répliquées, le kit reconstruit la page réelle du service (ex: Google, Microsoft) dans le navigateur de la victime en miroir, garantissant un aspect identique et permettant de passer outre les contrôles de sécurité classiques.
*   **Adaptabilité :** Les attaquants utilisent désormais des charges utiles multiples. Un même lien peut détecter la plateforme de la victime et proposer soit un phishing AiTM (pour voler une session), soit l'installation d'outils d'accès distant (RAT), soit des attaques de type *device code phishing*.

**Vulnérabilités :**
*   **DOMDIFFER :** Identifié comme le kit de phishing le plus performant entre août et octobre 2026. Il utilise le *DOM mirroring* pour cibler les comptes d'entreprise Microsoft et Google.
*   **Incontournables :** Les mécanismes de détection par réputation des domaines sont obsolètes car les attaquants renouvellent leurs noms de domaine très fréquemment et utilisent des techniques de masquage (*cloaking*) pour tromper les scanners de sécurité.

**Recommandations :**
*   **Déploiement de clés de sécurité (Passkeys) :** C'est la mesure la plus efficace pour contrer les attaques de type AiTM, car elles empêchent le vol de session, contrairement aux méthodes d'authentification par mot de passe ou code temporaire.
*   **Défense multicouche :** Ne pas se reposer uniquement sur les passerelles email. Mettre en place des solutions capables d'analyser le comportement des pages dans le navigateur et de détecter les changements de DOM suspects.
*   **Veille proactive :** Surveiller les nouvelles méthodes de relayage d'authentification, notamment les outils basés sur le *DOM mirroring* (ex: BlueKit, PhantomDOM, Laurseraph).

---
[Source](https://thehackernews.com/2026/11/most-wanted-phishing-kits-and.html){:target="_blank"}
