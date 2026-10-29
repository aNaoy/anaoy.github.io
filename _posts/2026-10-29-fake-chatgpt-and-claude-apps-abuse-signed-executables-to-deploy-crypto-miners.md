---
title: 'Fake ChatGPT and Claude Apps Abuse Signed Executables to Deploy Crypto Miners'
date: 2026-10-29
permalink: /posts/2026/10/29/fake-chatgpt-and-claude-apps-abuse-signed-executables-to-deploy-crypto-miners/
tags:
- veille-cyber
- hackernews
---
### Campagne Yoba : Des logiciels d'IA contrefaits diffusent des mineurs de cryptomonnaies

La campagne "Yoba" utilise des projets GitHub frauduleux promettant des applications de bureau basées sur ChatGPT et Claude pour infecter les systèmes des utilisateurs. En exploitant le référencement naturel (SEO poisoning), les attaquants attirent les cibles vers des téléchargements contenant un logiciel malveillant (YobaLoader) et un mineur de cryptomonnaies (XMRig).

**Points clés :**
*   **Technique de dissimulation :** Le malware utilise le *DLL sideloading* en combinant des exécutables légitimes et signés (OpenAI/Anthropic) avec des bibliothèques malveillantes.
*   **Contournement des défenses :** Les attaquants utilisent le DNS-over-HTTPS (DoH) pour masquer le trafic de commande et de contrôle (C2) et hébergent les charges utiles sur des plateformes de partage de fichiers légitimes.
*   **Mécanismes d'auto-protection :** Le malware inclut des délais d'exécution prolongés (plus de 12 jours par *Sleep*), des vérifications de hash pour garantir qu'il est lancé par l'exécutable prévu, et une exclusion géographique des pays issus de l'ex-URSS (sauf l'Ukraine).
*   **Persistance :** Le logiciel malveillant s'installe sur la machine via des tâches planifiées qui relancent régulièrement l'exécutable piégé.

**Vulnérabilités :**
*   Cette attaque n'exploite pas une faille logicielle spécifique (CVE), mais abuse de la confiance des utilisateurs dans les plateformes de développement (GitHub) et du mécanisme légitime de chargement de DLL de Windows.

**Recommandations :**
*   **Téléchargement officiel :** Ne téléchargez des outils d'IA ou des logiciels que depuis les sites officiels des éditeurs (openai.com, anthropic.com).
*   **Vigilance sur les résultats de recherche :** Soyez méfiant face aux résultats sponsorisés ou aux dépôts GitHub non officiels proposant des versions "desktop" ou "gratuites" de services d'IA renommés.
*   **Analyse comportementale :** Maintenez des solutions EDR/antivirus capables de détecter les comportements suspects (ex: lancement inhabituel de `svchost.exe` par un processus inconnu ou utilisation de minage de cryptomonnaies).
*   **Filtrage réseau :** Surveiller les requêtes DNS suspectes ou inhabituelles vers des domaines générés automatiquement (DGA) et les accès vers des sites de partage de fichiers non professionnels.

---
[Source](https://thehackernews.com/2026/10/fake-chatgpt-and-claude-apps-abuse.html){:target="_blank"}
