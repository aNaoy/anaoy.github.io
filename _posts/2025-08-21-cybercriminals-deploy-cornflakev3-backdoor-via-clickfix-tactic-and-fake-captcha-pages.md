---
title: 'Cybercriminals Deploy CORNFLAKE.V3 Backdoor via ClickFix Tactic and Fake CAPTCHA Pages'
date: 2025-08-21
permalink: /posts/2025/08/21/cybercriminals-deploy-cornflakev3-backdoor-via-clickfix-tactic-and-fake-captcha-pages/
tags:
- veille-cyber
- hackernews
---
### L'Ombre de CORNFLAKE.V3 : Une Campagne de Cybercriminalité Sophistiquée

Des acteurs malveillants exploitent une technique d'ingénierie sociale appelée "ClickFix" pour déployer une porte dérobée polyvalente nommée CORNFLAKE.V3. Cette campagne, suivie sous l'appellation UNC5518, s'inscrit dans une démarche de "accès en tant que service". Des pages CAPTCHA falsifiées servent d'appât pour inciter les utilisateurs à accorder un accès initial aux systèmes, qui est ensuite monétisé par d'autres groupes de menace.

L'infection initiale débute par le leurre d'utilisateurs sur des sites web compromis afin qu'ils copient et exécutent un script PowerShell malveillant via la boîte de dialogue "Exécuter" de Windows. L'accès ainsi obtenu est utilisé par au moins deux groupes distincts : UNC5774, pour déployer divers charges utiles, et UNC4108, pour installer des outils tels que VOLTMARKER et NetSupport RAT.

La chaîne d'attaque prend forme lorsqu'une victime, après avoir interagi avec des résultats de recherche manipulés (SEO poisoning ou publicités malveillantes), atterrit sur une page de vérification CAPTCHA frauduleuse. L'utilisateur est alors incité à exécuter une commande PowerShell malveillante. Ce dernier télécharge et exécute un script de deuxième étape qui vérifie l'environnement d'exécution et lance enfin CORNFLAKE.V3.

La porte dérobée CORNFLAKE.V3, observée en versions JavaScript et PHP, permet l'exécution de charges utiles diverses (exécutables, DLL, scripts) via HTTP et collecte des informations système basiques. Elle utilise le proxy Cloudflare Tunnel pour tenter d'échapper à la détection. Il s'agit d'une évolution de CORNFLAKE.V2, ajoutant la persistance via la clé de registre "Run" et supportant davantage de types de charges utiles. La persistance est assurée par des modifications du registre Windows.

Les charges utiles livrées incluent un outil de reconnaissance Active Directory, un script de collecte d'identifiants par Kerberoasting, et une autre porte dérobée nommée WINDYTWIST.SEA, capable de relayer le trafic TCP, d'offrir un shell inversé et d'exécuter des commandes. Certaines versions de WINDYTWIST.SEA ont également montré des tentatives de mouvement latéral au sein du réseau compromis.

Parallèlement, une campagne distincte utilise des clés USB pour infecter d'autres systèmes et déployer des mineurs de cryptomonnaies depuis septembre 2024. Cette méthode, peu coûteuse et contournant les sécurités réseau, implique l'exécution d'un raccourci (LNK) sur une clé USB infectée, déclenchant un script Visual Basic, puis un script batch. Ce processus lance des composants comme DIRTYBULK, CUTFAIL, HIGHREPS et PUMPBENCH. PUMPBENCH, une porte dérobée, facilite la reconnaissance, l'accès à distance via un serveur PostgreSQL, et le téléchargement de XMRig, un logiciel de minage de cryptomonnaies. PUMPBENCH propage également l'infection en infectant d'autres clés USB.

**Points Clés :**

*   **Tactic d'Ingénierie Sociale :** "ClickFix" et fausses pages CAPTCHA utilisées pour le leurre.
*   **Backdoor :** CORNFLAKE.V3 (évolution de V2) capable d'exécuter diverses charges utiles et d'établir la persistance.
*   **Services d'Accès :** Le groupe UNC5518 propose l'accès à d'autres groupes criminels (UNC5774, UNC4108).
*   **Charges Utiles Variées :** Outils de reconnaissance AD, Kerberoasting, WINDYTWIST.SEA, mineurs de cryptomonnaies (XMRig).
*   **Propagation :** Exploitation de failles via des scripts PowerShell et infection de clés USB.
*   **Obfuscation :** Utilisation de Cloudflare Tunnel pour masquer le trafic C2.

**Vulnérabilités Exploités (non spécifié dans l'article, mais le vecteur d'attaque est l'ingénierie sociale)**

**Recommandations :**

*   Désactiver la boîte de dialogue "Exécuter" de Windows lorsque possible pour atténuer l'exécution de malware via ClickFix.
*   Mener des exercices de simulation réguliers pour contrer les tactiques d'ingénierie sociale.
*   Mettre en place des systèmes de journalisation et de surveillance robustes pour détecter l'exécution de charges utiles ultérieures.
*   Sensibiliser les utilisateurs aux risques liés aux clics sur des liens suspects et à l'utilisation de clés USB inconnues.

---
[Source](https://thehackernews.com/2025/08/cybercriminals-deploy-cornflakev3.html){:target="_blank"}
