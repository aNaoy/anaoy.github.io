---
title: 'Malicious NGINX Configurations Enable Large-Scale Web Traffic Hijacking Campaign'
date: 2026-02-05
permalink: /posts/2026/02/05/malicious-nginx-configurations-enable-large-scale-web-traffic-hijacking-campaign/
tags:
- veille-cyber
- hackernews
---
## Campagne de Détournement de Trafic Web via Configurations NGINX Malveillantes

Des chercheurs en cybersécurité ont mis en lumière une campagne active de détournement de trafic web visant les installations NGINX et les panneaux de gestion tels que Baota (BT). Cette opération utilise des configurations NGINX malveillantes pour acheminer le trafic légitime vers des serveurs contrôlés par les attaquants. La campagne semble cibler spécifiquement les domaines asiatiques (.in, .id, .pe, .bd, .th), l'infrastructure d'hébergement chinoise (Baota Panel), ainsi que les domaines gouvernementaux et éducatifs (.edu, .gov).

L'attaque repose sur des scripts shell qui injectent des configurations NGINX altérées. Ces configurations, utilisant la directive `proxy_pass`, redirigent les requêtes entrantes sur des chemins d'URL prédéfinis vers des domaines sous le contrôle des acteurs malveillants. Le toolkit utilisé comprend plusieurs scripts :

*   **zx.sh** : Orchestre l'exécution des étapes suivantes.
*   **bt.sh** : Cible le Baota Management Panel pour écraser les fichiers de configuration NGINX.
*   **4zdh.sh** : Énumère les emplacements de configuration NGINX et minimise les erreurs lors de la création de nouvelles configurations.
*   **zdh.sh** : Se concentre sur les configurations NGINX sous Linux ou conteneurisées, ciblant les TLDs comme .in et .id.
*   **ok.sh** : Génère un rapport des règles de détournement de trafic NGINX actives.

Deux adresses IP, 193.142.147[.]209 et 87.121.84[.]24, sont identifiées comme étant responsables d'une majorité des tentatives d'exploitation observées.

**Points Clés :**

*   Détournement à grande échelle du trafic web via des configurations NGINX compromises.
*   Utilisation de scripts d'orchestration et d'injection de configurations malveillantes.
*   Ciblage de domaines spécifiques et de panneaux de gestion populaires.
*   Déploiement de charges utiles distinctes pour le minage de cryptomonnaies ou l'accès interactif.

**Vulnérabilités Mentionnées :**

*   Les attaques sont associées à l'exploitation de la vulnérabilité **React2Shell (CVE-2025-55182)**, avec un score CVSS de 10.0.

**Recommandations :**

Bien que l'article ne fournisse pas de recommandations explicites pour les utilisateurs finaux ou les administrateurs système, il est implicite que les mesures suivantes sont essentielles :

*   **Surveillance et sécurisation des configurations NGINX** : Examiner régulièrement les fichiers de configuration NGINX pour détecter toute modification suspecte ou non autorisée.
*   **Mise à jour des logiciels** : S'assurer que NGINX et les panneaux de gestion associés sont à jour pour corriger les vulnérabilités connues.
*   **Renforcement de la sécurité des serveurs** : Mettre en place des mesures de sécurité robustes pour les serveurs web et les environnements d'hébergement afin de prévenir les accès non autorisés et l'exécution de scripts malveillants.
*   **Segmentation du réseau et surveillance du trafic** : Mettre en place des mécanismes de détection et de prévention d'intrusion pour identifier et bloquer les activités suspectes.

---
[Source](https://thehackernews.com/2026/02/hackers-exploit-react2shell-to-hijack.html){:target="_blank"}
