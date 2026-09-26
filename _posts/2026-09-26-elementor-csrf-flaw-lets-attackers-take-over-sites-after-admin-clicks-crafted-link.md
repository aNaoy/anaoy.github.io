---
title: 'Elementor CSRF Flaw Lets Attackers Take Over Sites After Admin Clicks Crafted Link'
date: 2026-09-26
permalink: /posts/2026/09/26/elementor-csrf-flaw-lets-attackers-take-over-sites-after-admin-clicks-crafted-link/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique dans le plugin Elementor pour WordPress

Une faille de sécurité majeure (score CVSS 8.8) a été identifiée dans les versions 4.3.0 et 4.3.1 du plugin Elementor, affectant potentiellement plus de 2 millions de sites WordPress. Cette vulnérabilité de type CSRF (Cross-Site Request Forgery) permet à un attaquant non authentifié de prendre le contrôle total d'un site en incitant un administrateur connecté à cliquer sur un lien malveillant.

**Points clés :**
* **Mécanisme :** La faille réside dans le module « Editor Events », qui désactive la protection CSRF pour toute requête REST API contenant la chaîne de caractères « elementor/v1/events/ » dans son URI.
* **Impact :** Un attaquant peut contourner cette protection en ajoutant simplement ce paramètre à n'importe quelle requête REST API. Cela permet d'exécuter des actions critiques, notamment la création d'un compte administrateur pirate.
* **Accessibilité :** L'attaque ne nécessite aucune infrastructure complexe ; un simple lien intégré dans un e-mail ou un message suffit pour déclencher l'action si un administrateur clique dessus.

**Vulnérabilités :**
* Identifiant CVE : Non assigné.
* Type : Cross-Site Request Forgery (CSRF).
* Version affectée : Elementor 4.3.0 et 4.3.1.

**Recommandations :**
* **Mise à jour immédiate :** La vulnérabilité a été corrigée dans la version **4.3.2**. Il est impératif pour tous les administrateurs utilisant les versions 4.3.0 ou 4.3.1 de mettre à jour le plugin sans délai.

---
[Source](https://thehackernews.com/2026/09/elementor-csrf-flaw-lets-attackers-take.html){:target="_blank"}
