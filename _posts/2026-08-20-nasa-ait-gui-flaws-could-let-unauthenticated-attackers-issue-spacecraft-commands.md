---
title: 'NASA AIT-GUI Flaws Could Let Unauthenticated Attackers Issue Spacecraft Commands'
date: 2026-08-20
permalink: /posts/2026/08/20/nasa-ait-gui-flaws-could-let-unauthenticated-attackers-issue-spacecraft-commands/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans l'interface de contrôle NASA AIT-GUI

Des chercheurs en sécurité ont identifié une chaîne de vulnérabilités critiques dans **AIT-GUI**, l'interface web du kit d'outils AMMOS utilisé par la NASA pour le contrôle de ses engins spatiaux. Ces failles permettent à un attaquant non authentifié d'exécuter des commandes arbitraires sur les instruments et les systèmes de vol.

**Points clés :**
*   **Absence d'authentification :** L'interface génère automatiquement des cookies de session valides dès l'accès à la page racine, sans exiger de justificatifs.
*   **Risque opérationnel :** Un attaquant réseau peut envoyer des commandes vers le bus de contrôle, exécuter des scripts côté serveur ou manipuler des séquences de vol.
*   **Vecteur d'attaque :** La vulnérabilité est exploitable via des requêtes cross-origin (CSRF), permettant à un navigateur d'envoyer des commandes malveillantes sans interactions complexes.
*   **Remédiation incomplète :** Bien que la version 2.5.2 limite l'exposition réseau et bloque les requêtes cross-origin, l'absence d'authentification réelle persiste, rendant le système toujours vulnérable aux attaques directes.

**Vulnérabilités identifiées :**
*   **CVE-2026-60112 :** Défaut d'authentification critique permettant la création de sessions non autorisées et l'exécution de commandes (Score CVSS 9.3).
*   **GHSA-p9r8-2q67-fp86 :** Chaîne d'exploitation incluant CSRF, path traversal (CWE-22) et exécution arbitraire de commandes (Score CVSS 9.4).

**Recommandations :**
*   **Mise à jour :** Appliquer la version 2.5.2 au minimum pour limiter l'exposition aux attaques CSRF et restreindre l'écoute réseau.
*   **Isolation réseau :** Ne jamais exposer l'interface AIT-GUI sur des réseaux publics ou non sécurisés ; restreindre l'accès au niveau du pare-feu (bind limité à `localhost` recommandé).
*   **Vigilance continue :** Étant donné que l'authentification native reste absente, l'ajout d'une couche de contrôle d'accès externe (VPN, proxy inverse avec authentification robuste) est indispensable pour protéger les systèmes critiques.

---
[Source](https://thehackernews.com/2026/08/nasa-ait-gui-flaws-could-let.html){:target="_blank"}
