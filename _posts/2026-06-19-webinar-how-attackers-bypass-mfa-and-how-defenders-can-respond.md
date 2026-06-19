---
title: 'Webinar: How attackers bypass MFA and how defenders can respond'
date: 2026-06-19
permalink: /posts/2026/06/19/webinar-how-attackers-bypass-mfa-and-how-defenders-can-respond/
tags:
- veille-cyber
- bleepingcomp
---
### L'évolution des attaques par hameçonnage et le contournement de l'authentification multifacteur (MFA)

Face à l'efficacité croissante des protections traditionnelles, les attaquants délaissent le vol de mots de passe au profit de techniques détournant les flux d'authentification légitimes. Cette nouvelle menace, notamment illustrée par le "Device Code Phishing", permet aux cybercriminels d'obtenir des jetons d'accès persistants en manipulant les utilisateurs pour qu'ils valident eux-mêmes l'accès via des pages d'authentification Microsoft authentiques.

**Points clés :**
*   **Contournement de la MFA :** Les attaques modernes exploitent la confiance accordée aux services légitimes plutôt que de tenter de casser les protections.
*   **Persistance sans identifiants :** En utilisant des jetons d'accès au lieu de mots de passe, les attaquants échappent aux systèmes classiques de surveillance des identifiants.
*   **Limites des solutions actuelles :** Les outils de sécurité conventionnels peinent à détecter ces activités, car l'utilisateur effectue une procédure d'authentification réelle et valide.

**Vulnérabilités :**
*   L'article ne mentionne pas de CVE spécifique, car il se concentre sur l'exploitation abusive des processus d'authentification légitimes (OAuth, flux Device Code) plutôt que sur une faille logicielle traditionnelle.

**Recommandations :**
*   **Adoption de l'IA comportementale :** Utiliser des solutions basées sur l'analyse comportementale (UEBA) pour identifier les anomalies d'activité sur les comptes, invisibles pour les filtres classiques.
*   **Automatisation de la réponse :** Déployer des outils capables d'automatiser les investigations pour réduire le temps de réaction entre la compromission initiale et la remédiation.
*   **Sensibilisation ciblée :** Former les utilisateurs aux risques spécifiques liés aux demandes d'autorisation de code d'appareil (Device Code) et aux tentatives d'usurpation de flux de travail métier (BEC).

---
[Source](https://www.bleepingcomputer.com/news/security/webinar-how-attackers-bypass-mfa-and-how-defenders-can-respond/){:target="_blank"}
