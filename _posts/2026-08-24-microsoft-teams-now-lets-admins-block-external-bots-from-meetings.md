---
title: 'Microsoft Teams now lets admins block external bots from meetings'
date: 2026-08-24
permalink: /posts/2026/08/24/microsoft-teams-now-lets-admins-block-external-bots-from-meetings/
tags:
- veille-cyber
- bleepingcomp
---
### Sécurisation des réunions Microsoft Teams : blocage automatique des bots externes

Microsoft déploie une nouvelle fonctionnalité de sécurité permettant aux administrateurs de bloquer automatiquement la participation des bots externes aux réunions Teams. Cette mesure vise à limiter les risques d'intrusion, d'espionnage ou d'ingénierie sociale menés par des acteurs malveillants utilisant des bots automatisés.

**Points clés :**
* **Fonctionnalité :** Possibilité de bloquer systématiquement les bots identifiés sans intervention manuelle de l'organisateur.
* **Déploiement :** Disponibilité générale prévue pour fin septembre 2024.
* **Configuration :** L'option est désactivée par défaut dans le centre d'administration Teams sous « Gérer les bots ». Elle nécessite une activation explicite et peut être appliquée à des utilisateurs ou groupes spécifiques.
* **Contexte de menace :** Cette mesure répond à la recrudescence d'attaques exploitant Teams pour usurper l'identité de services IT, compromettre des réseaux ou diffuser des malwares.

**Vulnérabilités :**
* L'article ne mentionne pas de CVE spécifique, mais souligne l'exploitation croissante des fonctionnalités légitimes de Teams (bots, accès inter-locataires) pour des attaques d'ingénierie sociale et des déplacements latéraux au sein des réseaux d'entreprise.

**Recommandations :**
* **Activation de la protection :** Activer la nouvelle politique de blocage des bots externes dans le centre d'administration Teams dès sa disponibilité.
* **Gestion granulaire :** Appliquer les politiques de manière ciblée aux groupes les plus exposés ou manipulant des données sensibles.
* **Veille administrative :** Surveiller les futurs rapports d'audit et journaux de détection de bots que Microsoft prévoit d'introduire pour renforcer la visibilité sur les participants non humains.
* **Approche multicouche :** Compléter cette mesure avec le blocage des utilisateurs externes suspects via le portail Microsoft Defender pour se protéger contre les campagnes de phishing et d'usurpation d'identité.

---
[Source](https://www.bleepingcomputer.com/news/security/microsoft-teams-now-lets-admins-block-external-bots-from-meetings/){:target="_blank"}
