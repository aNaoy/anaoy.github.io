---
title: 'ThreatsDay Bulletin: DDR5 Bot Scalping, Samsung TV Tracking, Reddit Privacy Fine & More'
date: 2026-03-05
permalink: /posts/2026/03/05/threatsday-bulletin-ddr5-bot-scalping-samsung-tv-tracking-reddit-privacy-fine-more/
tags:
- veille-cyber
- hackernews
---
## Panorama de la Cybersécurité : Nouveaux Risques et Évolutions Réglementaires

Plusieurs développements récents mettent en lumière l'évolution constante du paysage des menaces en cybersécurité. Des campagnes de phishing sophistiquées, l'émergence de nouveaux outils malveillants, des changements dans les pratiques de collecte de données par de grandes entreprises, et des avancées technologiques impactant la vie privée sont au cœur des préoccupations.

**Points Clés et Vulnérabilités :**

*   **Campagnes de Phishing et Malware :** Des institutions gouvernementales ukrainiennes ont été ciblées par des e-mails contenant des archives ZIP ou des liens vers des sites vulnérables au XSS, distribuant les malwares SHADOWSNIFF, SALATSTEALER et le backdoor DEAFTICKK, attribués à l'acteur UAC-0252. Parallèlement, des campagnes soupçonnées d'espionnage russe auraient utilisé des malwares inédits comme BadPaw et MeowMeow. Un nouveau service de malware-as-a-service (MaaS), TrustConnect, se fait passer pour un outil de gestion et de surveillance à distance (RMM) et distribue un RAT (Remote Access Trojan) via des e-mails d'invitation ou de propositions commerciales frauduleuses. Des campagnes ont également intégré des logiciels RMM légitimes comme ScreenConnect et LogMeIn Resolve. Une version rebrandée, DocConnect, a émergé après des actions de perturbation. Le RAT TrustConnect permet un contrôle total des machines compromises.
    *   **Vulnérabilités :** L'exploitation de vulnérabilités dans les pratiques de sécurité des utilisateurs via le phishing et l'ingénierie sociale. L'utilisation de malwares d'extraction d'informations et de backdoors.

*   **Suivi par les Capteurs de Pression des Pneus (TPMS) :** Les capteurs TPMS émettent des signaux sans chiffrement contenant des identifiants uniques persistants, permettant le suivi et la reconnaissance des véhicules. Cela ouvre la voie à un réseau de surveillance discret et à faible coût, utilisant des récepteurs SDR pour collecter des données sur les déplacements de milliers de véhicules. Des utilisateurs malveillants pourraient déployer ces récepteurs à grande échelle pour suivre des individus sans leur connaissance, collectant des informations potentiellement sensibles.
    *   **Vulnérabilités :** Conception des TPMS permettant la diffusion d'identifiants persistants sans chiffrement.

*   **Plateformes de Cybercriminalité et Outils Malveillants :**
    *   **Telegram :** La plateforme est devenue un hub central pour les cybercriminels, facilitant la coordination des opérations, la monétisation, la publicité, le recrutement d'affiliés et la croissance de leur audience, remplaçant de plus en plus les écosystèmes basés sur Tor.
    *   **AuraStealer :** Des analyses ont révélé 48 noms de domaine de commande et de contrôle (C2) liés aux opérations d'AuraStealer. Le groupe utilise des domaines .shop et .cfd et achemine le trafic via Cloudflare comme proxy inverse. Ce stealer, apparu après la perturbation de Lumma Stealer, est proposé sous forme d'abonnement et distribué via des campagnes comme ClickFix.
    *   **Atomic Stealer (Malext) :** Une campagne de malvertising utilise de fausses publicités sur Google pour rediriger les utilisateurs vers des pages frauduleuses (Medium, Evernote, Kimi AI) proposant des solutions pour libérer de l'espace de stockage sur macOS. Ces pages diffusent des instructions de type ClickFix qui déploient une nouvelle variante de l'Atomic Stealer, nommée Malext, pour voler des données. La campagne exploite plus de 50 comptes Google Ads compromis.
    *   **Agent Tesla :** Une campagne de phishing, utilisant des leurres de bons de commande, déploie un Agent Tesla via une chaîne d'attaque multi-étapes. L'objectif est de collecter des données sensibles tout en utilisant des techniques d'obfuscation et d'exécution en mémoire pour échapper à la détection. Le malware intègre des mécanismes anti-analyse.
        *   **Vulnérabilités :** Utilisation de plateformes de messagerie pour la coordination des attaques, exploitation de domaines compromis, diffusion via des fausses publicités et des e-mails de phishing, techniques d'évasion avancées.

*   **Bots et Grattage de Données :** Plus de 10 millions de requêtes de web scraping ont été effectuées pour cibler les pages de produits DRAM sur des sites e-commerce afin de trouver des vendeurs disposant de stocks de mémoire DDR5. Ces bots vérifient le stock toutes les 6,5 secondes, utilisent des techniques de cache busting et ajustent leur vitesse pour éviter la détection. Ils exacerbent la pénurie de composants pour des reventes profitables, éloignant les clients légitimes et augmentant les prix.
    *   **Vulnérabilités :** Exploitation des pages produits en ligne pour le scalping de matériel informatique.

*   **Abus des Domaines .arpa :** Des acteurs malveillants exploitent le domaine de premier niveau .arpa, réservé à l'infrastructure réseau, pour héberger du contenu malveillant et contourner les listes de blocage traditionnelles. Ce comportement démontre la recherche de lieux de stockage "impossibles" au sein de l'infrastructure fondamentale de l'internet. De plus, des fichiers raccourcis LNK et le protocole WebDAV sont utilisés pour télécharger des fichiers malveillants sur les systèmes cibles, profitant de la faible connaissance de la fonctionnalité d'accès à distance via l'Explorateur de fichiers.
    *   **Vulnérabilités :** Exploitation de la réserve de l'espace .arpa pour des activités malveillantes, utilisation de LNK et WebDAV pour la distribution de malware.

*   **Désanonymisation par IA :** Des modèles de langage volumineux (LLM) ont été développés pour désanonymiser les utilisateurs d'Internet en se basant sur d'anciens commentaires ou d'autres indices numériques. Cette méthode permet d'extraire des caractéristiques pertinentes, de rechercher des correspondances via des plongements sémantiques et de vérifier les correspondances, même si les cibles utilisent différents pseudonymes sur plusieurs plateformes. Cette automatisation de la désanonymisation remet en cause l'hypothèse de pseudonymat comme protection adéquate de la vie privée en ligne.
    *   **Vulnérabilités :** L'utilisation des LLM pour automatiser la désanonymisation d'individus sur Internet.

**Recommandations et Évolutions :**

*   **Google Chrome :** Le cycle de publication des nouvelles versions de Chrome passe à deux semaines, au lieu de quatre. Cela vise à fournir aux développeurs et aux utilisateurs un accès plus rapide aux améliorations de performance, aux correctifs et aux nouvelles fonctionnalités. Les mises à jour de sécurité continueront d'être livrées chaque semaine.
    *   **Recommandation :** Maintenir Chrome à jour pour bénéficier des correctifs de sécurité et des nouvelles fonctionnalités.

*   **Lutte contre le Scalping de RAM :** Les mesures visant à limiter le scalping de composants informatiques par des bots sont nécessaires pour assurer un accès équitable aux produits pour les consommateurs légitimes.

*   **Confidentialité des Données des Consommateurs :**
    *   **Reddit :** La plateforme a été condamnée à une amende de 14,47 millions de livres sterling par l'ICO britannique pour traitement illégal des données personnelles d'enfants et pour ne pas avoir correctement vérifié l'âge de ses utilisateurs, les exposant à des contenus inappropriés.
        *   **Recommandation :** Les plateformes doivent renforcer leurs mesures de vérification d'âge et de protection des données des mineurs.
    *   **Samsung :** Le procureur général du Texas a obtenu un accord avec Samsung stipulant que la collecte de données ACR (Automated Content Recognition) sur les téléviseurs intelligents ne pourra se faire qu'avec le consentement exprès des consommateurs. Samsung devra mettre à jour ses téléviseurs avec des écrans de divulgation et de consentement clairs.
        *   **Recommandation :** Les fabricants de dispositifs connectés doivent être transparents sur leurs pratiques de collecte de données et obtenir un consentement éclairé.

*   **Sécurité des Appareils Mobiles :**
    *   **Apple :** Les iPhones et iPads d'Apple ont été approuvés pour traiter des informations classifiées dans les réseaux de l'OTAN, devenant les premiers appareils grand public à être autorisés sans logiciel ou paramètres spéciaux supplémentaires.
    *   **TikTok :** La plateforme a déclaré qu'elle n'ajouterait pas le chiffrement de bout en bout aux messages directs, car cela empêcherait les forces de l'ordre et les équipes de sécurité d'accéder aux messages si nécessaire.
        *   **Recommandation :** Les utilisateurs doivent être conscients des politiques de confidentialité et de sécurité des plateformes qu'ils utilisent.

*   **Prudence avec les Agents de Codage IA :** Il est conseillé de ne pas déléguer aveuglément le jugement, l'architecture et la validation à un seul modèle d'IA. Les IA peuvent reproduire des faiblesses existantes et peuvent ne pas toujours identifier de manière fiable les vulnérabilités exploitables dans des environnements complexes. Il est déconseillé d'utiliser le même système d'IA pour la rédaction et la revue de code.
    *   **Recommandation :** Maintenir une supervision humaine dans le processus de développement logiciel, même lors de l'utilisation d'outils d'IA.

*   **Protection contre le Phishing :** Une campagne de phishing cible les utilisateurs de LastPass en utilisant des leurres liés à un accès non autorisé à leur compte. Elle exploite le fait que de nombreux clients d'e-mail n'affichent que le nom d'affichage, masquant l'adresse réelle de l'expéditeur. Les attaquants réexpédient de fausses chaînes d'e-mails pour usurper l'identité de LastPass.
    *   **Recommandation :** Soyez vigilant face aux e-mails suspects, vérifiez toujours l'adresse de l'expéditeur et ne cliquez pas sur les liens dans les e-mails non sollicités.

Dans l'ensemble, ces développements soulignent la nécessité d'une vigilance constante et d'une adaptation continue face aux menaces évolutives et aux nouvelles technologies.

---
[Source](https://thehackernews.com/2026/03/threatsday-bulletin-redis-rce-ddr5-bot.html){:target="_blank"}
