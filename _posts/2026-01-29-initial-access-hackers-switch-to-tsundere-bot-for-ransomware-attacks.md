---
title: 'Initial access hackers switch to Tsundere Bot for ransomware attacks'
date: 2026-01-29
permalink: /posts/2026/01/29/initial-access-hackers-switch-to-tsundere-bot-for-ransomware-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### L'Évolution des Tactiques des Attaquants Initiaux : Tsundere Bot et XWorm

Des acteurs malveillants, identifiés sous le nom de TA584, intensifient leurs activités d'accès initial en utilisant une combinaison du logiciel malveillant Tsundere Bot et du cheval de Troie d'accès à distance XWorm. Cette approche, qui échappe aux détections statiques, vise à établir un accès réseau susceptible de mener à des attaques par ransomware. TA584, actif depuis 2020, a vu ses opérations tripler fin 2025, élargissant sa portée géographique au-delà de l'Amérique du Nord et du Royaume-Uni/Irlande pour inclure l'Allemagne, plusieurs pays européens et l'Australie.

La chaîne d'attaque actuelle débute par des courriels envoyés depuis des comptes compromis via des services comme SendGrid et Amazon SES. Ces messages contiennent des URL uniques, des mécanismes de géolocalisation et de filtrage IP, ainsi que des redirections impliquant des systèmes de direction de trafic tiers. Les victimes qui franchissent ces premières étapes sont dirigées vers une page CAPTCHA, suivie d'une page "ClickFix" qui incite l'utilisateur à exécuter une commande PowerShell. Cette commande télécharge et exécute un script obfusqué qui charge XWorm ou Tsundere Bot en mémoire, avant de rediriger le navigateur vers un site inoffensif pour tromper l'utilisateur.

Tsundere Bot est une plateforme de type "malware-as-a-service" dotée de capacités de porte dérobée et de chargement. Il nécessite l'installation de Node.js sur le système de la victime. La localisation de ses serveurs de commande et de contrôle (C2) s'effectue via la blockchain Ethereum, utilisant une technique similaire à EtherHiding, avec une adresse de repli intégrée dans l'installateur. Le logiciel malveillant communique via WebSockets et évite de s'exécuter sur des systèmes configurés dans des langues des pays de la CEI (Communauté des États Indépendants), principalement le russe. Il collecte des informations sur le système, peut exécuter du code JavaScript arbitraire et est capable d'utiliser les machines compromises comme proxies SOCKS. La plateforme Tsundere Bot intègre également un marché pour la vente et l'achat de bots.

Les chercheurs prévoient que TA584 continuera à explorer de nouvelles cibles et à expérimenter avec différents types de charges utiles.

**Points Clés :**

*   **Acteur de Menace :** TA584
*   **Outils Principaux :** Tsundere Bot et XWorm RAT
*   **Objectif :** Accès initial menant potentiellement à des attaques par ransomware.
*   **Méthode de Distribution :** Campagnes d'emailing massives via des comptes compromis, utilisant des URL uniques, des filtres et des pages trompeuses (CAPTCHA, ClickFix).
*   **Technologie de Tsundere Bot :** Nécessite Node.js, utilise la blockchain Ethereum pour la localisation C2, communique via WebSockets, évite les systèmes CEI, collecte des informations système, exécute du code arbitraire, agit comme proxy, et possède un marché intégré.
*   **Évolution :** Augmentation significative des activités, expansion géographique, et évasion des détections statiques.

**Vulnérabilités :**

Aucune vulnérabilité spécifique (CVE) n'est explicitement mentionnée dans l'article pour les logiciels malveillants eux-mêmes. Cependant, l'article met en évidence l'exploitation de la confiance des utilisateurs via des techniques d'ingénierie sociale (CTAs, fausses pages) et l'utilisation d'outils légitimes (PowerShell) dans la chaîne d'attaque. La vulnérabilité réside dans le manque de vigilance des utilisateurs face aux e-mails de phishing et à l'exécution de commandes non sollicitées.

**Recommandations :**

*   **Sensibilisation et Formation des Utilisateurs :** Éduquer les employés à reconnaître les e-mails de phishing, à ne pas cliquer sur des liens suspects ou à télécharger des pièces jointes non sollicitées, et à se méfier des demandes d'exécution de commandes.
*   **Filtrage des E-mails :** Renforcer les solutions de sécurité des e-mails pour détecter et bloquer les e-mails malveillants, y compris ceux provenant de services légitimes mais compromis.
*   **Gestion des Accès et des Privilèges :** Mettre en œuvre le principe du moindre privilège pour limiter les dommages potentiels en cas d'infection.
*   **Surveillance et Détection :** Utiliser des solutions de sécurité avancées capables de détecter les comportements suspects et les menaces de type "fileless" (comme le chargement en mémoire).
*   **Mises à Jour Régulières :** Maintenir les systèmes d'exploitation et les logiciels à jour pour corriger les vulnérabilités connues. Bien que non spécifié, les environnements avec Node.js devraient être particulièrement surveillés.
*   **Segmentation Réseau :** Limiter la propagation latérale des menaces en segmentant le réseau.

---
[Source](https://www.bleepingcomputer.com/news/security/initial-access-hackers-switch-to-tsundere-bot-for-ransomware-attacks/){:target="_blank"}
