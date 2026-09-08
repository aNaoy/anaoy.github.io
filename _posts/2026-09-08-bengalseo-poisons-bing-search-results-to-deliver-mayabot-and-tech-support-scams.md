---
title: 'BengalSEO Poisons Bing Search Results to Deliver MayaBot and Tech Support Scams'
date: 2026-09-08
permalink: /posts/2026/09/08/bengalseo-poisons-bing-search-results-to-deliver-mayabot-and-tech-support-scams/
tags:
- veille-cyber
- hackernews
---
### BengalSEO : Une menace persistante par empoisonnement SEO

La campagne **BengalSEO**, active depuis 2015 et opérée depuis le Rajasthan (Inde), utilise des techniques avancées de référencement malveillant pour piéger les utilisateurs de Microsoft Bing. Ce groupe utilise une infrastructure complexe pour rediriger les victimes vers des logiciels malveillants ou des centres d'appels frauduleux.

**Points clés :**
*   **Mode opératoire :** Les attaquants créent de fausses pages de support technique ou de téléchargement logiciel (ex: Bitdefender, Vizio). Ils utilisent des techniques de "Black Hat SEO" (bourrage de mots-clés, injection DOM, création massive de backlinks) pour apparaître en tête des résultats de recherche.
*   **Infection :** Les victimes sont redirigées via un système de distribution de trafic (TDS) qui filtre les robots de sécurité et trace les utilisateurs via *Matomo*.
*   **Payload :** Le logiciel malveillant principal, **MayaBot**, assure le contrôle à distance (C2), le monitoring système et l'installation d'un mineur de cryptomonnaie (XMRig).
*   **Infrastructure :** Le groupe détourne la réputation de plateformes légitimes (GitHub, ReadTheDocs, Google Sites) pour héberger ses pages leurres et maintenir ses campagnes.

**Vulnérabilités exploitées :**
*   L'article ne mentionne pas de CVE spécifique, mais souligne une **exploitation détournée de la confiance accordée aux plateformes d'hébergement légitimes** et une manipulation des algorithmes de classement des moteurs de recherche via l'abus de contenus générés par les utilisateurs (UGC).

**Recommandations :**
*   **Vérification des sources :** Méfiez-vous des premiers résultats de recherche pour les portails de support technique ou d'activation de services ; préférez accéder directement aux sites officiels en saisissant l'URL dans la barre d'adresse.
*   **Prudence avec les téléchargements :** Évitez de télécharger des exécutables à partir de pages trouvées via des liens sponsorisés ou des résultats de recherche non vérifiés, surtout s'ils sont hébergés sur des plateformes de partage de code (GitHub, etc.).
*   **Analyse comportementale :** Les utilisateurs doivent être alertés par des instructions invitant à appeler un numéro de support technique ou par le comportement inhabituel de leur navigateur (redirections multiples, temps de latence avant téléchargement).
*   **Sécurité des sites :** Les propriétaires de sites web doivent surveiller régulièrement leur propre référencement et s'assurer que leur infrastructure n'est pas utilisée pour de l'hébergement de spam ou des redirections illicites.

---
[Source](https://thehackernews.com/2026/09/bengalseo-poisons-bing-search-results.html){:target="_blank"}
