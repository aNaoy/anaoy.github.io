---
title: 'We Built An Agent That Broke All of Our Security Rules. Heres What We Learned.'
date: 2026-11-11
permalink: /posts/2026/11/11/we-built-an-agent-that-broke-all-of-our-security-rules-heres-what-we-learned/
tags:
- veille-cyber
- hackernews
---
### Sécurisation des agents IA : Les risques de l'usurpation de session humaine

L'utilisation d'agents IA interagissant via les sessions authentifiées des utilisateurs pose un problème majeur de sécurité : les applications sont incapables de distinguer les actions d'un agent de celles d'un humain, l'agent héritant des privilèges totaux de la session utilisateur.

**Points clés**
* **Absence de distinction :** Les agents basés sur le navigateur opèrent avec les identifiants et les droits de l'utilisateur, rendant leurs actions indiscernables dans les journaux d'audit.
* **Complexité des standards :** Bien que des initiatives comme *WebMCP* (pour définir des actions d'outils) et *Web Bot Auth* (pour signer les requêtes) soient en cours, aucune solution ne lie actuellement l'identité de l'agent, le mandat de l'utilisateur (délégation) et la portée de la tâche.
* **Risque opérationnel :** Sans une gestion explicite des autorisations, les agents deviennent un vecteur rapide d'abus de privilèges.

**Vulnérabilités**
* **Invisibilité contextuelle :** L'application ne peut pas vérifier si une action est initiée par l'humain ou l'agent.
* **Délégation non restreinte :** Par défaut, l'agent possède la portée totale de la session utilisateur, dépassant le besoin réel de la tâche.
* **Absence de traçabilité séparée :** Le manque de signature spécifique pour les actions d'agent empêche l'audit différencié. 
*(Note : Aucune CVE spécifique n'est mentionnée, car il s'agit d'une problématique de conception architecturale et non d'une faille logicielle isolée).*

**Recommandations pour les équipes de sécurité**
* **Inventaire actif :** Recenser systématiquement les extensions et agents de navigateur capables d'agir au sein des sessions authentifiées.
* **Audit de privilèges :** Mapper les agents aux utilisateurs et revoir les accès associés à chaque entité.
* **Mise en place de "Step-up Authentication" :** Exiger une validation humaine supplémentaire (passkey, confirmation) pour les actions critiques ou irréversibles.
* **Exigence de transparence auprès des SaaS :** Interroger les fournisseurs de logiciels sur leur capacité à distinguer, dans les journaux d'audit, l'activité humaine de celle des agents.
* **Principe du moindre privilège :** Restreindre les capacités des agents au sein de l'interface (ex: mode lecture seule par défaut, blocage des formulaires sensibles).

---
[Source](https://thehackernews.com/2026/11/we-built-agent-that-broke-all-of-our.html){:target="_blank"}
