---
title: 'Calendar Invites and Live Proxies: Inside a Google Session Hijacking Campaign'
date: 2026-11-12
permalink: /posts/2026/11/12/calendar-invites-and-live-proxies-inside-a-google-session-hijacking-campaign/
tags:
- veille-cyber
- hackernews
---
### Opération CloudFire : Piratage de sessions Google via des invitations calendrier

Une vaste campagne de phishing sophistiquée, identifiée sous le nom d'**Opération CloudFire**, a ciblé des utilisateurs professionnels pour dérober des sessions Google actives. Plutôt que de simples identifiants, cette méthode intercepte les jetons de session en temps réel, contournant ainsi l'authentification multifacteur (MFA).

**Points clés :**
* **Vecteur d'attaque :** Utilisation d'invitations Google Calendar et de partages Drive provenant de comptes compromis au sein de relations de confiance existantes.
* **Mécanisme :** Emploi de proxys inverses (via le framework **Nyasher**) qui se placent devant la page de connexion réelle de Google pour capturer les mots de passe et les jetons MFA en temps réel.
* **Contournement des défenses :** Les attaquants exploitent les redirecteurs légitimes de Google et génèrent des pages de phishing dynamiques (non statiques) qui échappent aux scanners de sécurité traditionnels.
* **Infrastructure jetable :** Rotation rapide de domaines fraîchement enregistrés et utilisation de certificats émis juste avant l'attaque pour éviter les systèmes de réputation.
* **Impact :** Une fois la session capturée, l'attaquant accède aux emails, fichiers Drive et peut accorder des permissions OAuth persistantes.

**Vulnérabilités :**
Il n'existe pas de CVE spécifique, car l'attaque repose sur une **ingénierie sociale** ciblée et une exploitation légitime des services Google (Open Redirects) couplée à des proxys transparents. Le framework utilisé est connu sous le nom de **Nyasher**.

**Recommandations :**
* **Approche multicritère :** Ne pas se fier à un seul indicateur (réputation de domaine ou lien). Croiser systématiquement le contexte de l'expéditeur, l'intention réelle du message et l'analyse technique des sauts.
* **Surveillance des logs :** Auditer étroitement les journaux Google Workspace pour détecter des accès inhabituels, des révocations de sessions suspectes ou des octrois de permissions OAuth.
* **Gestion des sessions :** Réduire le temps de validité des sessions et disposer de capacités de réponse rapide pour révoquer les accès en moins d'une heure en cas de compromission.
* **Traiter le Calendrier comme une surface d'attaque :** Appliquer des filtres de sécurité aux invitations calendrier et pas seulement aux emails.
* **Action sur l'infrastructure :** Collaborer avec les plateformes (comme Cloudflare Abuse) pour faire tomber les domaines et serveurs backend utilisés pour le proxing, plutôt que de tenter uniquement de bloquer les emails un par un.

---
[Source](https://thehackernews.com/2026/11/calendar-invites-and-live-proxies.html){:target="_blank"}
