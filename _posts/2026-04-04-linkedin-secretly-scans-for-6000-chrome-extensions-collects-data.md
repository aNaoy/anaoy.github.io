---
title: 'LinkedIn secretly scans for 6,000+ Chrome extensions, collects data'
date: 2026-04-04
permalink: /posts/2026/04/04/linkedin-secretly-scans-for-6000-chrome-extensions-collects-data/
tags:
- veille-cyber
- bleepingcomp
---
### BrowserGate : Le pistage des extensions par LinkedIn

LinkedIn déploie des scripts JavaScript furtifs capables d'identifier plus de 6 000 extensions installées sur les navigateurs basés sur Chromium de ses utilisateurs. Ce procédé, baptisé « BrowserGate », permet à la plateforme de collecter des empreintes numériques détaillées (fingerprinting), incluant la configuration matérielle, le fuseau horaire et les outils tiers utilisés par l'internaute.

**Points clés :**
* **Collecte de données :** LinkedIn vérifie la présence d'extensions spécifiques en accédant aux ressources statiques de celles-ci. Le nombre d'extensions ciblées a considérablement augmenté ces dernières années, passant de 2 000 à plus de 6 000.
* **Motivations divergentes :** Le rapport « BrowserGate » accuse LinkedIn de récolter ces données pour identifier les entreprises utilisant des outils concurrents et appliquer des mesures restrictives. À l'inverse, LinkedIn affirme que cette pratique vise uniquement à protéger sa plateforme contre le *scraping* (extraction automatisée de données) et à garantir sa stabilité technique.
* **Pratique répandue :** Le fingerprinting à des fins de sécurité ou de lutte contre la fraude est une technique déjà observée chez d'autres grandes entreprises (eBay, banques, etc.).

**Vulnérabilités :**
* Aucune CVE n'est associée, car il s'agit d'une utilisation intentionnelle de fonctionnalités standards des navigateurs. La vulnérabilité réside dans l'exploitation de mécanismes de détection par ressources statiques qui permettent le pistage d'utilisateurs sans leur consentement explicite.

**Recommandations :**
* **Utilisation de navigateurs axés sur la confidentialité :** Privilégier des navigateurs intégrant des protections natives contre le *fingerprinting* (ex: Brave, Mullvad Browser ou Firefox avec des réglages durcis).
* **Extensions de protection :** Installer des bloqueurs de scripts ou des extensions de confidentialité (ex: uBlock Origin, Privacy Badger) capables de restreindre l'exécution de scripts tiers.
* **Gestion des extensions :** Limiter le nombre d'extensions installées sur le navigateur pour réduire la surface d'exposition aux techniques de profilage.
* **Contrôle des permissions :** Inspecter régulièrement les autorisations accordées aux extensions installées et supprimer celles qui ne sont plus nécessaires.

---
[Source](https://www.bleepingcomputer.com/news/security/linkedin-secretly-scans-for-6-000-plus-chrome-extensions-collects-data/){:target="_blank"}
