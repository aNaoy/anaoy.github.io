---
title: 'US Becomes Top Target in RMM Phishing Campaign Spanning 46 Countries'
date: 2026-09-03
permalink: /posts/2026/09/03/us-becomes-top-target-in-rmm-phishing-campaign-spanning-46-countries/
tags:
- veille-cyber
- hackernews
---
### Campagne mondiale de phishing basée sur l'abus de logiciels RMM

Une vaste campagne de phishing, touchant 46 pays, utilise des logiciels légitimes de surveillance et de gestion à distance (RMM) pour compromettre des systèmes. Les États-Unis sont la cible principale, concentrant 45 % des activités détectées.

**Points clés :**
* **Infrastructures éphémères :** Les attaquants font pivoter quotidiennement leurs infrastructures (94 % des hôtes ne sont actifs qu'une journée), utilisant des services tels que Vercel, GitHub Pages, Netlify et divers espaces de stockage cloud.
* **Techniques de leurre :** Utilisation de documents falsifiés variés (avis fiscaux, factures, communications de transporteurs type UPS, documents de sécurité sociale) pour inciter les victimes à installer des outils RMM.
* **Secteurs visés :** Éducation, technologie, gouvernement, banque, finance et industrie.
* **Persistance malgré la rotation :** Bien que les domaines changent, le "kit" de phishing conserve des empreintes digitales stables (fichiers de police spécifiques, structure de livraison `secure.html` vers `project/*.zip`).

**Vulnérabilités :**
Cette menace n'exploite pas une CVE spécifique, mais repose sur l'**abus de fonctionnalités légitimes** de logiciels RMM et la détournement de services cloud de confiance pour contourner les défenses périmétriques traditionnelles.

**Recommandations pour les équipes SOC :**
* **Défense agnostique :** Ne pas se limiter à la surveillance d'un logiciel RMM spécifique, mais se concentrer sur la chaîne de livraison et les comportements d'accès à distance non autorisés.
* **Analyse comportementale :** Prioriser la détection des indicateurs persistants (structure de la chaîne de phishing, ressources partagées) plutôt que celle des domaines ou adresses IP, qui sont trop éphémères.
* **Contrôles au niveau des emails :** Renforcer la vigilance face aux archives protégées par mot de passe.
* **Contextualisation :** Utiliser des bacs à sable (sandboxes) interactifs pour obtenir une visibilité complète sur le comportement des scripts, les téléchargements et l'activité réseau en temps réel.

---
[Source](https://thehackernews.com/2026/09/us-becomes-top-target-in-rmm-phishing.html){:target="_blank"}
