---
title: 'Google Chrome to warn users before opening insecure HTTP sites'
date: 2025-10-28
permalink: /posts/2025/10/28/google-chrome-to-warn-users-before-opening-insecure-http-sites/
tags:
- veille-cyber
- bleepingcomp
---
**Chrome Renforce la Sécurité par Défaut des Connexions Web**

Dès octobre 2026, avec la version 154, Google Chrome demandera par défaut l'autorisation de l'utilisateur avant d'accéder à des sites web publics utilisant le protocole HTTP non sécurisé. Cette mesure vise à prévenir les attaques de type "man-in-the-middle" qui exploitent la transmission de données non chiffrées.

Auparavant, une option similaire "Toujours utiliser les connexions sécurisées" existait mais devait être activée manuellement. Désormais, elle sera activée par défaut pour les sites publics. Chrome n'affichera l'avertissement que lors du premier accès à un nouveau site HTTP ou s'il est rarement visité, évitant ainsi une surcharge d'alertes pour les utilisateurs fréquentant des sites sécurisés.

Les utilisateurs pourront choisir d'étendre ces alertes aux sites privés, bien que ces derniers soient généralement considérés comme moins exposés aux risques d'attaques externes. Cette évolution s'inscrit dans la tendance générale d'adoption du protocole HTTPS, dont le taux est passé d'environ 30-45% en 2015 à 95-99% actuellement.

Avant le déploiement général, cette fonctionnalité sera testée sur plus d'un milliard d'utilisateurs bénéficiant de la protection Enhanced Safe Browsing dès avril 2026 (Chrome 147). Les développeurs et professionnels de l'informatique sont encouragés à migrer leurs sites vers HTTPS dès maintenant. Cette initiative fait suite à d'autres améliorations récentes, comme la mise à niveau automatique vers HTTPS pour les liens en page et la révocation des permissions de notification pour les sites inactifs.

**Points Clés :**

*   **Changement de comportement par défaut :** Chrome demandera l'autorisation avant d'accéder à des sites HTTP publics à partir d'octobre 2026 (Chrome 154).
*   **Objectif :** Protéger les utilisateurs des attaques "man-in-the-middle" en favorisant le protocole HTTPS sécurisé.
*   **Gestion des alertes :** Les avertissements seront ciblés sur les nouveaux sites HTTP ou ceux peu visités pour éviter la saturation.
*   **Options de personnalisation :** Possibilité d'étendre les alertes aux sites privés.
*   **Déploiement progressif :** Phase de test auprès des utilisateurs d'Enhanced Safe Browsing en avril 2026 (Chrome 147).

**Vulnérabilités (implicites, non liées à des CVE spécifiques dans cet article) :**

*   **Attaques Man-in-the-Middle (MITM) :** Les connexions HTTP non chiffrées permettent à des attaquants d'intercepter et de modifier les données échangées entre l'utilisateur et le serveur.
*   **Exposition aux malwares et au hameçonnage :** Les sites HTTP peuvent être détournés pour distribuer des logiciels malveillants ou mener des actions d'ingénierie sociale.

**Recommandations :**

*   **Pour les utilisateurs :** Examiner attentivement les avertissements de Chrome concernant les sites non sécurisés et privilégier l'utilisation de connexions HTTPS.
*   **Pour les développeurs et professionnels de l'informatique :** Migrer les sites web vers le protocole HTTPS pour assurer la sécurité des utilisateurs et se conformer aux futures exigences du navigateur.

---
[Source](https://www.bleepingcomputer.com/news/google/google-chrome-to-warn-users-before-opening-insecure-http-sites/){:target="_blank"}
