---
title: 'OpenAI Revokes macOS App Certificate After Malicious Axios Supply Chain Incident'
date: 2026-04-13
permalink: /posts/2026/04/13/openai-revokes-macos-app-certificate-after-malicious-axios-supply-chain-incident/
tags:
- veille-cyber
- hackernews
---
### Compromission de la chaîne d'approvisionnement logicielle : L'incident OpenAI et la menace TeamPCP

OpenAI a récemment révoqué un certificat de signature pour ses applications macOS suite à l'utilisation, dans un workflow GitHub Actions, d'une version compromise de la bibliothèque **Axios** (versions 1.14.1 et 0.30.4). Bien qu'aucune donnée utilisateur ou système interne n'ait été compromise, OpenAI a agi par précaution en révoquant le certificat, rendant obsolètes les anciennes versions de ses applications de bureau à partir du 8 mai 2026.

Cet incident s'inscrit dans une campagne de grande ampleur menée par le groupe **TeamPCP** (UNC6780), qui a multiplié les attaques par empoisonnement de dépendances (Axios, Trivy, LiteLLM, Telnyx). Ces attaques visent à dérober des identifiants et à déployer des malwares (backdoor WAVESHAPER.V2, infostealer SANDCLOCK, trojan via DonutLoader) au sein des environnements CI/CD.

**Vulnérabilités clés :**
*   **CVE-2026-33634 :** Identifiant associé à la campagne de compromission des outils de sécurité et des workflows (ex: Trivy, LiteLLM).
*   **Vecteurs d'attaque :** Injection de malwares dans les workflows GitHub Actions, utilisation de packages npm/PyPI empoisonnés et vol d'identifiants au sein des pipelines CI/CD.

**Points clés :**
*   **Impact étendu :** Des centaines de milliers d'identifiants dérobés circulent, facilitant des intrusions dans des environnements cloud (ex: Commission européenne, Mercor).
*   **Évolution des tactiques :** TeamPCP utilise désormais des techniques avancées comme la stéganographie (WAV) et des logiciels malveillants multi-plateformes.
*   **Ciblage des outils de sécurité :** Le choix des attaquants s'est porté sur des outils privilégiés (scanners, SDK) afin de maximiser leur accès au sein des organisations.

**Recommandations de sécurité :**
*   **Fiabilisation des dépendances :** Verrouiller les packages par leur condensat (digest) ou SHA de commit plutôt que par des tags mutables.
*   **Durcissement des CI/CD :** Traiter chaque exécuteur de workflow comme un point de compromission potentiel ; éviter les triggers `pull_request_target` inutiles.
*   **Gestion des accès :** Utiliser des identifiants à courte durée de vie et à portée restreinte (Least Privilege).
*   **Infrastructure :** Déployer des miroirs internes ou des proxys d'artefacts, et utiliser le "Trusted Publishing" pour les publications de packages.
*   **Monitoring :** Déployer des jetons de type "canary" pour détecter les tentatives d'exfiltration et auditer régulièrement les secrets codés en dur.

---
[Source](https://thehackernews.com/2026/04/openai-revokes-macos-app-certificate.html){:target="_blank"}
