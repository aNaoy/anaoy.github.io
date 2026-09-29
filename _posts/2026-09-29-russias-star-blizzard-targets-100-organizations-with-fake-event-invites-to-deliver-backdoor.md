---
title: 'Russias Star Blizzard Targets 100+ Organizations With Fake Event Invites to Deliver Backdoor'
date: 2026-09-29
permalink: /posts/2026/09/29/russias-star-blizzard-targets-100-organizations-with-fake-event-invites-to-deliver-backdoor/
tags:
- veille-cyber
- hackernews
---
### Campagne de cyberespionnage du groupe Star Blizzard : Infiltrations via des invitations factices

Le groupe de hackers russe **Star Blizzard** (lié au FSB) mène des campagnes de spear-phishing sophistiquées ciblant plus de 100 organisations, principalement aux États-Unis et au Royaume-Uni, impliquées dans des sujets liés à l'Ukraine. Les attaquants utilisent des invitations factices à des événements prestigieux pour déployer le backdoor **CosmicPulse**.

#### Points clés
*   **Tactiques d'ingénierie sociale :** Utilisation d'invitations usurpant des institutions réputées (Chatham House, Atlantic Council) ou des communications internes. Les échanges initiaux par e-mail visent à instaurer la confiance avant l'envoi d'archives protégées par mot de passe.
*   **Évolution technique (RedFlick) :** Le groupe utilise désormais des tâches planifiées Windows (déguisées en composants système) pour installer ses outils malveillants, remplaçant les anciennes méthodes basées sur des CAPTCHA factices.
*   **Vecteurs d'infection :** L'attaque repose sur des fichiers LNK malveillants déguisés en PDF qui, une fois ouverts, exécutent des scripts pour télécharger le malware via des services comme SSH ou le protocole WebDAV.
*   **Polyvalence des menaces :** En plus de *CosmicPulse*, des variantes ont été observées utilisant *DarkSword*, un kit d'exploitation ciblant les iPhone.

#### Vulnérabilités ciblées
*   **iOS :** Le kit d'exploitation *DarkSword* tire profit de 6 vulnérabilités distinctes sur iPhone (corrigées à partir de la version iOS 26.3).
*   **Défauts humains :** La confiance accordée aux e-mails imitant des sources légitimes et l'ouverture de pièces jointes non sollicitées.

#### Recommandations de sécurité
*   **Détection et traque :**
    *   Rechercher les noms de tâches planifiées suspicieuses : *Internet Quality Test Connection*, *Network Configuration Manager* et *System Health Monitor*.
    *   Surveiller les détections Microsoft Defender : `Trojan:Script/RedFlick` et `Backdoor:Python/CosmicPulse`.
    *   Conserver les journaux de logs au-delà de 7 jours (via Microsoft Sentinel par exemple) pour une analyse rétrospective.
*   **Durcissement (Hardening) :**
    *   Restreindre les connexions SSH sortantes non autorisées.
    *   Activer les règles de réduction de la surface d'attaque (ASR) de Microsoft Defender pour bloquer les exécutables suspects et les scripts obfusqués.
*   **Protection des accès :** Privilégier les méthodes d'authentification résistantes au phishing (clés FIDO2/WebAuthn), car le groupe utilise *Evilginx* pour contourner l'authentification multifacteur (MFA) classique en volant les cookies de session.
*   **Hygiène logicielle :** Mettre à jour les terminaux iOS vers la version 26.3 ou supérieure et activer le « mode isolement » (Lockdown Mode) si nécessaire.
*   **Vérification :** En cas de doute sur un e-mail, confirmer l'invitation par un canal de communication officiel et connu (téléphone ou e-mail habituel).

---
[Source](https://thehackernews.com/2026/09/russias-star-blizzard-targets-100.html){:target="_blank"}
