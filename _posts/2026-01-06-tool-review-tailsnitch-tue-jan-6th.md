---
title: 'Tool Review: Tailsnitch, (Tue, Jan 6th)'
date: 2026-01-06
permalink: /posts/2026/01/06/tool-review-tailsnitch-tue-jan-6th/
tags:
- veille-cyber
- sans-isc
---
**Tailsnitch : Audit de Configurations Tailscale**

Tailsnitch est un nouvel outil open-source développé par Adversis pour auditer la sécurité des configurations Tailscale. Tailscale est une solution de réseau superposé basé sur Wireguard, simplifiant la connexion directe entre appareils, y compris ceux derrière des NAT. Bien que Tailscale soit facile à utiliser, des erreurs de configuration peuvent entraîner l'exposition involontaire de ressources internes. Tailsnitch vise à identifier ces problèmes et à suggérer des améliorations.

**Points Clés :**

*   **Fonctionnalité :** Tailsnitch scanne les configurations Tailscale pour détecter les vulnérabilités et les points faibles.
*   **Facilité d'utilisation :** L'outil est simple à exécuter, notamment via une interface en ligne de commande. Il peut s'authentifier via des identifiants OAUTH.
*   **Découverte de fonctionnalités :** L'outil aide également à découvrir et comprendre des fonctionnalités avancées de Tailscale pour un meilleur durcissement de la sécurité.
*   **Rapports détaillés :** Les résultats sont présentés avec des niveaux de gravité (information, faible, moyen, critique) et fournissent les détails nécessaires pour la remédiation.

**Vulnérabilités Identifiées (Exemples rencontrés par l'auteur) :**

*   Versions obsolètes de Tailscale sur certains systèmes.
*   Utilisation de clés d'authentification sans expiration (présenté comme un risque acceptable par l'utilisateur pour un usage personnel limité).
*   Absence de définition de règles ACL (Access Control List).

*(Aucun CVE spécifique n'est mentionné dans l'article pour les configurations Tailscale.)*

**Recommandations :**

*   Utiliser Tailsnitch pour vérifier régulièrement la sécurité de vos configurations Tailscale.
*   Mettre à jour les clients Tailscale vers les dernières versions.
*   Explorer et configurer les règles ACL pour un contrôle d'accès plus précis.
*   Revoir et gérer les durées de vie des clés d'authentification, surtout dans des environnements partagés ou sensibles.
*   Considérer l'activation de fonctionnalités de sécurité avancées proposées par Tailscale, dont certaines peuvent nécessiter un compte payant.

---
[Source](https://isc.sans.edu/diary/rss/32602){:target="_blank"}
