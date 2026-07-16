---
title: '20+ Hijacked Government Websites Became an Attack Channel'
date: 2026-07-16
permalink: /posts/2026/07/16/20-hijacked-government-websites-becamean-attack-channel/
tags:
- veille-cyber
- hackernews
---
### La campagne PhantomEnigma : détournement d'infrastructures gouvernementales

La campagne **PhantomEnigma** exploite plus de 20 sites web officiels brésiliens (.gov.br) pour diffuser des logiciels malveillants. En utilisant des infrastructures de confiance et des emails authentifiés (passant les protocoles SPF, DKIM et DMARC), les attaquants contournent les mécanismes de sécurité classiques pour piéger les institutions financières et les organismes publics.

#### Points clés
*   **Mode opératoire :** Utilisation de documents falsifiés (convocations policières, procurations) envoyés par emails compromis ou via des liens redirigeant vers des domaines gouvernementaux piratés.
*   **Évolution :** La menace a muté, passant de logiciels malveillants bancaires basés sur des extensions de navigateur à une architecture modulaire complexe (Backdoor index.js).
*   **Modularité :** Le logiciel malveillant utilise des applications Electron légitimes détournées pour charger une porte dérobée capable d'exécuter du JavaScript, de télécharger des charges utiles secondaires (stealers, loaders, outils de gestion à distance) et de persister sur le système.
*   **Évasion :** L'usage de domaines de confiance et de serveurs de commande et contrôle (C2) tournants rend les listes de blocage statiques inefficaces.

#### Vulnérabilités
*   **Abus d'infrastructure :** Exploitation de serveurs web gouvernementaux légitimes comme relais de confiance pour la redirection de trafic malveillant.
*   **Détournement d'applications :** Utilisation d'applications légitimes (ex: Boostnote) modifiées pour exécuter des scripts malveillants via `eval()`.
*   *Note : Aucune CVE spécifique n'est mentionnée, la campagne s'appuyant sur des accès compromis et l'ingénierie sociale plutôt que sur l'exploitation directe de failles logicielles documentées.*

#### Recommandations
*   **Analyse comportementale :** Privilégier la détection basée sur le comportement des processus plutôt que sur des signatures statiques (IP, domaines), en raison de la rotation constante des infrastructures.
*   **Threat Hunting :** Mettre en œuvre une surveillance continue pour identifier les accès suspects aux endpoints et les connexions réseau sortantes vers des C2 inconnus.
*   **Sensibilisation :** Établir des procédures permettant aux employés de signaler les messages officiels suspects afin d'être analysés par les équipes de sécurité, même lorsqu'ils proviennent de sources perçues comme fiables.
*   **Validation :** Renforcer la vigilance face aux documents officiels (PDF/QR codes) reçus par email, même si les checks de messagerie (DMARC/SPF/DKIM) sont valides.

---
[Source](https://thehackernews.com/2026/07/20-hijacked-government-websites.html){:target="_blank"}
