---
title: 'Lazarus Deploys RemotePE Memory-Only RAT Against Financial and Crypto Firms'
date: 2026-05-25
permalink: /posts/2026/05/25/lazarus-deploys-remotepe-memory-only-rat-against-financial-and-crypto-firms/
tags:
- veille-cyber
- hackernews
---
### Menace persistante : Le malware RemotePE utilisé par le groupe Lazarus

Le groupe Lazarus, lié à la Corée du Nord, déploie un cheval de Troie d'accès à distance (RAT) sophistiqué baptisé **RemotePE** pour cibler des organisations du secteur financier et des cryptomonnaies. Ce malware se distingue par son exécution exclusivement en mémoire, ne laissant aucune trace sur le système de fichiers pour échapper aux outils de détection traditionnels.

#### Points clés
*   **Chaîne d'infection en trois étapes :**
    1.  **DPAPILoader :** Déchiffre et charge le composant suivant via l'API DPAPI de Windows.
    2.  **RemotePELoader :** Établit une connexion avec le serveur de commande et contrôle (C2) via HTTP et récupère le module principal.
    3.  **RemotePE :** RAT complet capable d'exécuter des commandes à distance (gestion de processus, manipulation de fichiers, configuration C2).
*   **Techniques d'évasion :** Utilisation de *Hell’s Gate* pour masquer les appels système et neutralisation du suivi d'événements Windows (ETW).
*   **Méthodes d'attaque :** Utilisation de l'ingénierie sociale via Telegram (usurpation d'identité, faux domaines de prise de rendez-vous) pour compromettre les appareils des employés.
*   **Persistance :** Conçu pour une surveillance à long terme avant de passer à des objectifs à fort impact (vol de données ou détournement de fonds).

#### Vulnérabilités
Aucune CVE spécifique n'est exploitée ; le malware repose sur l'exploitation humaine (ingénierie sociale) et sur des techniques avancées d'évasion EDR (Endpoint Detection and Response) pour contourner les défenses existantes sans nécessiter de vulnérabilité logicielle logicielle classique.

#### Recommandations
*   **Sensibilisation :** Former les employés aux risques de l'ingénierie sociale, particulièrement sur les plateformes comme Telegram, et à la vigilance concernant les liens vers des outils de planification (Calendly, Picktime).
*   **Surveillance réseau :** Surveiller les communications sortantes vers des domaines suspects ou non identifiés et renforcer l'inspection du trafic HTTPS.
*   **Détection comportementale :** Privilégier les solutions EDR capables d'analyser les comportements en mémoire et de détecter des anomalies telles que le patching d'ETW ou des appels API inhabituels.
*   **Zero Trust :** Appliquer les principes du moindre privilège pour limiter l'impact potentiel d'une compromission initiale d'un poste de travail.

---
[Source](https://thehackernews.com/2026/05/lazarus-deploys-remotepe-memory-only.html){:target="_blank"}
