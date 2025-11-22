---
title: 'Matrix Push C2 Uses Browser Notifications for Fileless, Cross-Platform Phishing Attacks'
date: 2025-11-22
permalink: /posts/2025/11/22/matrix-push-c2-uses-browser-notifications-for-fileless-cross-platform-phishing-attacks/
tags:
- veille-cyber
- hackernews
---
## L'Avènement de Matrix Push C2 : Phishing Fileless via Notifications Navigateur

Une nouvelle plateforme de commande et contrôle (C2) baptisée "Matrix Push C2" exploite les notifications des navigateurs web pour mener des attaques de phishing fileless et multiplateformes. Ces attaques visent à tromper les utilisateurs en les amenant à autoriser les notifications de sites malveillants ou compromis. Une fois l'autorisation accordée, les attaquants utilisent le mécanisme natif des notifications push pour afficher des alertes d'apparence légitime, imitant des messages du système d'exploitation ou du navigateur. Ces fausses notifications contiennent des liens qui, une fois cliqués, redirigent les victimes vers des sites frauduleux.

Cette méthode contourne les mesures de sécurité traditionnelles car elle n'implique pas d'infection initiale du système. La nature inter-navigateur de l'attaque la rend efficace sur tous les systèmes d'exploitation. Matrix Push C2 est proposé comme un service de malware (MaaS) via des canaux de cybercriminalité, avec des abonnements mensuels, trimestriels, semestriels et annuels. La plateforme web inclut un tableau de bord pour envoyer des notifications, suivre les victimes, créer des liens raccourcis, et potentiellement enregistrer des extensions de navigateur, y compris des portefeuilles de cryptomonnaies. Les messages de phishing sont personnalisables pour usurper l'identité d'entreprises connues telles que MetaMask, Netflix, Cloudflare, PayPal et TikTok. Le but final peut être le vol de données, de credentials, ou la compromission de portefeuilles de cryptomonnaies.

Parallèlement, une augmentation des attaques utilisant l'outil légitime de forensics et de réponse aux incidents, Velociraptor, a été observée. Ces attaques exploitent souvent des vulnérabilités logicielles, comme la faille CVE-2025-59287 dans Windows Server Update Services, pour obtenir un accès initial et mener des activités de reconnaissance. Cela démontre la tendance des acteurs malveillants à utiliser des outils open-source et légitimes à des fins offensives.

**Points Clés:**

*   **Nouvelle plateforme C2 :** Matrix Push C2 utilise les notifications des navigateurs pour des attaques de phishing.
*   **Approche Fileless :** Aucune infection directe du système n'est nécessaire, l'attaque se déroule dans le navigateur.
*   **Multiplateforme :** Efficace sur tous les systèmes d'exploitation disposant d'un navigateur compatible.
*   **Ingénierie Sociale :** Les victimes sont incitées à autoriser les notifications via de fausses alertes.
*   **Malware-as-a-Service (MaaS) :** La plateforme est vendue sous forme d'abonnement.
*   **Usurpation d'identité :** Utilisation de marques connues pour gagner en crédibilité.
*   **Objectifs :** Vol de données, credentials, cryptomonnaies, installation de malware plus persistant.
*   **Utilisation d'outils légitimes :** Augmentation des attaques utilisant des outils de DFIR comme Velociraptor.

**Vulnérabilités:**

*   **CVE-2025-59287 :** Vulnérabilité dans Windows Server Update Services (score CVSS : 9.8) exploitée pour obtenir un accès initial dans certaines attaques utilisant Velociraptor.

**Recommandations:**

*   **Vigilance accrue :** Méfiance envers les notifications de sites web, surtout celles demandant des actions immédiates ou des vérifications.
*   **Contrôle des autorisations de notification :** Examiner et révoquer régulièrement les autorisations de notification des sites web dans les paramètres du navigateur.
*   **Sensibilisation à l'ingénierie sociale :** Former les utilisateurs à reconnaître les tactiques d'ingénierie sociale et les tentatives de phishing.
*   **Mises à jour régulières :** Maintenir les systèmes d'exploitation, les navigateurs et les autres logiciels à jour pour corriger les vulnérabilités connues.
*   **Solutions de sécurité :** Utiliser des solutions de sécurité endpoint (EDR/XDR) et des filtres web pour détecter et bloquer les activités suspectes.
*   **Analyse des outils :** Les entreprises de cybersécurité doivent surveiller l'utilisation abusive d'outils légitimes par les acteurs malveillants.

---
[Source](https://thehackernews.com/2025/11/matrix-push-c2-uses-browser.html){:target="_blank"}
