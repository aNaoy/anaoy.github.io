---
title: 'Iranian Hackers Deploy MiniFast and MiniJunk V2 via Phishing and SEO Poisoning'
date: 2026-05-26
permalink: /posts/2026/05/26/iranian-hackers-deploy-minifast-and-minijunk-v2-via-phishing-and-seo-poisoning/
tags:
- veille-cyber
- hackernews
---
### Escalade des cyberattaques iraniennes : l'utilisation de l'IA et de l'empoisonnement SEO

Le groupe de hackers affilié à l'État iranien, **Nimbus Manticore** (UNC1549), a intensifié ses opérations d'espionnage industriel depuis février 2026, ciblant les secteurs de l'aviation, de l'énergie et du logiciel aux États-Unis, en Europe et au Moyen-Orient. Le groupe innove en utilisant l'IA générative pour accélérer le développement de ses outils malveillants.

**Points clés :**
*   **Diversification des vecteurs :** Passage du phishing classique (fausses offres d'emploi) à l'empoisonnement SEO pour diffuser des logiciels piégés.
*   **Techniques d'infection :** Utilisation du détournement de DLL (*AppDomain hijacking*) pour déployer des charges utiles.
*   **Cibles critiques :** Espionnage d'entreprises du secteur pétrolier et gazier, et intrusions dans des systèmes de surveillance de réservoirs (ATG) aux États-Unis via des accès exposés.

**Vulnérabilités et vecteurs d'attaque :**
*   **MiniFast (MiniUpdate) & MiniJunk V2 :** Nouveaux backdoors persistants permettant l'exécution de commandes à distance, l'exfiltration de fichiers et l'élévation de privilèges (*runas*).
*   **AppDomain Hijacking :** Exploitation de la méthode de chargement des DLL par Windows pour exécuter du code arbitraire via des applications légitimes.
*   **Exposition critique :** Systèmes de gestion de réservoirs (ATG) connectés à Internet sans protection par mot de passe.
*   **Note CVE :** Aucune CVE spécifique n'est mentionnée, les attaques reposent sur des techniques d'ingénierie sociale et des détournements de fonctionnalités système légitimes.

**Recommandations :**
*   **Vigilance logicielle :** Télécharger les outils de développement (type SQL Developer) uniquement depuis les sites officiels des éditeurs et éviter les liens sponsorisés ou les résultats de recherche douteux.
*   **Renforcement des accès :** Sécuriser impérativement tous les dispositifs industriels (IoT, ATG) connectés à Internet par des mots de passe robustes et les isoler derrière des VPN ou des pare-feu.
*   **Sensibilisation :** Former les employés à la méfiance vis-à-vis des invitations de réunions (Zoom, Teams) ou des offres d'emploi non sollicitées, méthodes favorites du groupe pour l'accès initial.
*   **Gestion des DLL :** Surveiller les comportements anormaux des applications légitimes (appels réseau, exécutions de processus enfants inhabituels) pour détecter le détournement de DLL.

---
[Source](https://thehackernews.com/2026/05/iranian-hackers-deploy-minifast-and.html){:target="_blank"}
