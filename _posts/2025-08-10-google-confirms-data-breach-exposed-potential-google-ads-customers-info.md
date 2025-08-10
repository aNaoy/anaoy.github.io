---
title: 'Google confirms data breach exposed potential Google Ads customers info'
date: 2025-08-10
permalink: /posts/2025/08/10/google-confirms-data-breach-exposed-potential-google-ads-customers-info/
tags:
- veille-cyber
- bleepingcomp
---
**Fuite d'informations clients chez Google Ads**

Google a reconnu qu'une faille de sécurité touchant une instance de Salesforce a entraîné l'exposition d'informations concernant des clients potentiels de Google Ads. Les données compromises incluent des noms d'entreprises, des numéros de téléphone et des notes internes destinées aux commerciaux de Google. Les informations de paiement et les données des comptes Google Ads ne sont pas affectées.

Cette attaque a été menée par des acteurs malveillants identifiés comme ShinyHunters, en collaboration avec Scattered Spider, qui seraient responsables de l'accès initial aux systèmes. Les attaquants utilisent des techniques d'ingénierie sociale et des applications OAuth compromises pour accéder aux données. Les groupes de pirates se font désormais appeler "Sp1d3rHunters".

Les acteurs de la menace auraient demandé une rançon à Google pour ne pas divulguer les données volées. Ils ont également développé de nouveaux outils pour faciliter l'exfiltration de données depuis les instances Salesforce compromises, en utilisant notamment des scripts Python à la place du Salesforce Data Loader.

**Points clés:**

*   **Incident:** Fuite de données affectant des clients potentiels de Google Ads.
*   **Données exposées:** Noms d'entreprises, numéros de téléphone, notes internes de commerciaux.
*   **Données non affectées:** Informations de paiement, données des comptes Google Ads (Google Ads Account, Merchant Center, Google Analytics).
*   **Acteurs de la menace:** ShinyHunters et Scattered Spider (qui se présentent sous le nom de "Sp1d3rHunters").
*   **Méthode d'attaque:** Compromission des instances Salesforce via ingénierie sociale et applications OAuth malveillantes.
*   **Tentative d'extorsion:** Demande de rançon pour la non-divulgation des données volées.
*   **Nouvelles techniques:** Utilisation de scripts Python pour faciliter l'exfiltration de données.

**Vulnérabilités mentionnées:**

*   Pas de CVE spécifique mentionné dans l'article. L'accès semble avoir été obtenu par des attaques de phishing et l'abus d'applications OAuth Salesforce.

**Recommandations implicites (non explicitement formulées mais déduites de l'article):**

*   **Renforcement de la sécurité des instances CRM:** Mettre en place des mesures de sécurité robustes pour protéger les données stockées dans les systèmes CRM comme Salesforce.
*   **Sensibilisation des employés:** Former le personnel aux risques d'ingénierie sociale et aux techniques de phishing.
*   **Surveillance des applications tierces:** Vérifier attentivement les autorisations accordées aux applications tierces connectées aux systèmes critiques.
*   **Mise à jour des outils et des protocoles de sécurité:** Se tenir informé des nouvelles méthodes d'attaque et adapter les défenses en conséquence, notamment en ce qui concerne les outils d'accès aux données.

---
[Source](https://www.bleepingcomputer.com/news/security/google-confirms-data-breach-exposed-potential-google-ads-customers-info/){:target="_blank"}
