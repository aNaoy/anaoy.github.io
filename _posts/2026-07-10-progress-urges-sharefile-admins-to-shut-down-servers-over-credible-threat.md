---
title: 'Progress urges ShareFile admins to shut down servers over “credible” threat'
date: 2026-07-10
permalink: /posts/2026/07/10/progress-urges-sharefile-admins-to-shut-down-servers-over-credible-threat/
tags:
- veille-cyber
- bleepingcomp
---
# Menace critique sur les serveurs ShareFile de Progress Software

Progress Software a émis une alerte de sécurité urgente concernant ses *Storage Zone Controllers* (serveurs Windows locaux utilisés dans les déploiements hybrides de ShareFile). La société a identifié une menace externe crédible ciblant ces composants, incitant à une mise hors service immédiate des serveurs concernés pour protéger les données.

**Points clés**
* **Cible :** Les *Storage Zone Controllers* hébergés sur site (on-premise) qui servent d'interface entre les infrastructures locales et la plateforme cloud de ShareFile.
* **Nature de la menace :** Une vulnérabilité ou une campagne d'attaque non spécifiée visant directement les serveurs exposés à Internet.
* **Statut actuel :** Progress a temporairement désactivé l'accès via son cloud, mais souligne que cette mesure est insuffisante pour garantir la sécurité.
* **Historique :** Le contexte rappelle les attaques par exploitation de vulnérabilités « zero-day » survenues par le passé sur d'autres solutions de transfert de fichiers de Progress (ex: MOVEit).

**Vulnérabilités**
* Aucune CVE n'a été communiquée à ce stade par Progress Software, l'enquête étant toujours en cours.

**Recommandations**
* **Arrêt immédiat :** Les administrateurs doivent éteindre manuellement les serveurs Windows hébergeant les *Storage Zone Controllers*.
* **Veille active :** Surveiller les communications officielles de Progress Software pour toute mise à jour ou procédure de remédiation à venir sous 24 heures.
* **Prudence :** Ne pas redémarrer les services tant qu'une déclaration officielle de sécurité n'aura pas confirmé la résolution de la menace.

---
[Source](https://www.bleepingcomputer.com/news/security/progress-urges-sharefile-customers-to-shut-down-servers-over-credible-threat/){:target="_blank"}
