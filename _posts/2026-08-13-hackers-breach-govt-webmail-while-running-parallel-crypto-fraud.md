---
title: 'Hackers breach govt webmail while running parallel crypto fraud'
date: 2026-08-13
permalink: /posts/2026/08/13/hackers-breach-govt-webmail-while-running-parallel-crypto-fraud/
tags:
- veille-cyber
- bleepingcomp
---
### Espionnage d'État et fraude crypto : Le double visage du groupe Jewelbug

Le groupe de hackers chinois **Jewelbug** (aussi nommé Earth Alux ou REF7707) mène une vaste campagne hybride combinant cyber-espionnage gouvernemental et opérations de fraude aux cryptomonnaies à l'échelle industrielle.

#### Points clés
*   **Mode opératoire :** Le groupe a compromis une plateforme d'hébergement web mutualisée, accédant ainsi aux services de webmail de 15 entités gouvernementales. En injectant un script malveillant dans les modèles de pages, ils capturent les sessions et identifient les cibles de haute valeur.
*   **Outils d'espionnage :** Déploiement du backdoor **Antino** via de faux installateurs Adobe Flash, et utilisation d'une extension de navigateur malveillante nommée "PDF Viewer" pour voler des cookies, des identifiants et intercepter le trafic.
*   **Infrastructure malveillante :** Utilisation de Google Docs pour héberger des charges utiles, et exploitation de serveurs Linux/ARM64/routeurs ASUS via l'implant **ClientKing** (basé sur Rust).
*   **Fraude financière :** Utilisation d'IA générative pour créer des sites de phishing (imitation d'OKX et Binance) et de bots de "click-fraud" pour manipuler le référencement naturel (SEO) et attirer les victimes.
*   **Volume des données :** Plus d'un million d'implantations, 580 000 cookies volés et des milliers de courriels exfiltrés.

#### Vulnérabilités
Bien que l'article ne mentionne pas de CVE spécifique, l'attaque repose sur :
*   **Injection de script (XSS persistant) :** Modification des templates de serveurs web partagés.
*   **Défaut de ségrégation des privilèges :** La compromission d'une plateforme d'hébergement centrale a permis une attaque "supply chain" impactant de multiples locataires (tenants) gouvernementaux.

#### Recommandations
*   **Sécurisation des hébergements :** Renforcer l'isolation entre les environnements de webmail mutualisés pour éviter qu'une compromission sur un serveur ne se propage à l'ensemble des locataires.
*   **Contrôle des extensions :** Restreindre strictement l'installation d'extensions de navigateur sur les postes de travail administratifs via des politiques de groupe (GPO).
*   **Surveillance des logs :** Auditer régulièrement les flux de connexion sortants vers des services publics (comme Google Docs) utilisés comme serveurs C2 pour masquer le trafic.
*   **Sensibilisation :** Alerter les utilisateurs sur les faux messages de mise à jour (Adobe Flash est obsolète et ne devrait plus faire l'objet de mises à jour via des pop-ups web).
*   **Analyse SEO :** Surveiller les campagnes de recherche pour identifier les sites frauduleux utilisant des techniques de manipulation de classement pour usurper l'identité de services financiers officiels.

---
[Source](https://www.bleepingcomputer.com/news/security/hackers-breach-govt-webmail-while-running-parallel-crypto-fraud/){:target="_blank"}
