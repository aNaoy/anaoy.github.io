---
title: 'CERT-In Flags AI-Driven Attacks as Backdoored ARTEX Exposes 62 Consoles to Root Access'
date: 2026-11-05
permalink: /posts/2026/11/05/cert-in-flags-ai-driven-attacks-as-backdoored-artex-exposes-62-consoles-to-root-access/
tags:
- veille-cyber
- hackernews
---
### Menace de "Crafty Falcon" : L'IA au service de cyberattaques et backdoors critiques

Le CERT-In alerte sur les activités du groupe "Crafty Falcon", qui utilise des outils offensifs dopés à l'IA (ARTEX, PentAGI, CyberStrikeAI) pour automatiser des attaques rapides et adaptatives contre les secteurs financiers (BFSI) et les plateformes de cryptomonnaies.

**Points clés :**
*   **Vitesse et autonomie :** Les outils d'IA exécutent des chaînes d'attaque complètes, créent des scripts personnalisés en temps réel et pivotent rapidement pour éviter la détection.
*   **Vecteurs d'accès :** Exploitation d'API exposées, de jetons statiques codés en dur, de dépôts de code compromis et absence de MFA sur les services critiques.
*   **Contournement des contrôles :** Les attaquants volent des identifiants API légitimes pour effectuer des transferts de fonds directement via l'infrastructure autorisée de la victime, neutralisant ainsi les contrôles de sécurité métier (KYC, plafonds, etc.).
*   **Backdoor massive :** Des copies malveillantes de l'outil open-source **ARTEX** sur Docker Hub injectent une porte dérobée (root shell) non authentifiée, compromettant 62 consoles identifiées publiquement.

**Vulnérabilités :**
*   **Porte dérobée dans ARTEX (tomicdd/artex et congdonglinux/artex) :** Injection d'une fonction `verifyCaptcha()` détournée permettant une exécution de commande en tant que `root` sans authentification préalable.
*   **Exploitation logicielle :** Vulnérabilités de type *file-upload* et *deserialization* dans des applications PHP et Node.js.

**Recommandations :**
*   **Gouvernance IA :** Appliquer le cadre d'audit du CERT-In, notamment le principe du moindre privilège (PoLP) et l'exigence d'une approbation humaine pour toute action critique réalisée par une IA.
*   **Sécurisation des outils :** Éviter l'utilisation d'outils de sécurité non audités ou téléchargés depuis des sources non fiables. Vérifier l'intégrité des images Docker.
*   **Hygiène des accès :** Supprimer les jetons d'API statiques et les identifiants codés en dur. Imposer le MFA sur toutes les applications et terminaux distants.
*   **Surveillance :** Mettre en place une surveillance continue des journaux API et des flux financiers pour détecter les transactions de test (micro-valeurs) et les appels non autorisés.
*   **Infrastructure :** Isoler les environnements de production des environnements de non-production pour limiter les mouvements latéraux.

---
[Source](https://thehackernews.com/2026/11/backdoored-docker-image-for-artex-ai.html){:target="_blank"}
