---
title: 'The Back Door Attackers Know About — and Most Security Teams Still Haven’t Closed'
date: 2026-05-05
permalink: /posts/2026/05/05/the-back-door-attackers-know-about-and-most-security-teams-still-havent-closed/
tags:
- veille-cyber
- hackernews
---
### La menace invisible des jetons OAuth persistants

Les jetons OAuth, utilisés par les applications tierces (IA, outils d'automatisation) pour se connecter aux environnements Google ou Microsoft, représentent une faille de sécurité majeure et persistante. Contrairement aux mots de passe, ces jetons n'expirent pas, ne sont pas réinitialisés lors d'un changement de compte et permettent de contourner totalement l'authentification multifacteur (MFA).

**Points clés :**
* **Invisibilité périmétrique :** Les contrôles de sécurité classiques ne détectent pas l'usage de jetons légitimes.
* **Le risque "Supply Chain" :** L'incident Drift a démontré que des attaquants peuvent détourner les jetons d'applications tierces pourtant dignes de confiance pour infiltrer des centaines d'organisations.
* **Carence opérationnelle :** Bien que 80 % des responsables sécurité identifient ce risque comme critique, 45 % ne déploient aucune surveillance active, se contentant souvent de suivis manuels inefficaces.

**Vulnérabilités :**
* Absence d'expiration automatique des jetons d'accès et de rafraîchissement OAuth.
* Manque de visibilité centralisée sur les permissions accordées par les utilisateurs.
* **CVE :** Aucune CVE spécifique n'est mentionnée, car il s'agit d'un problème lié à la conception même du protocole OAuth et à son usage à grande échelle, plutôt qu'à une faille logicielle isolée.

**Recommandations :**
* **Surveillance comportementale continue :** Ne pas se limiter à l'analyse des permissions lors de l'installation, mais monitorer en temps réel les appels API effectués par les applications.
* **Évaluation du « rayon d'explosion » (Blast Radius) :** Prioriser la surveillance des jetons associés à des comptes disposant d'accès sensibles (VIP, administrateurs).
* **Réponse automatisée graduée :** Mettre en place des mécanismes de révocation automatique pour les activités hautement anormales, tout en conservant une intervention humaine pour les intégrations critiques.
* **Visibilité globale :** Adopter des solutions capables d'auditer l'intégralité des connexions OAuth existantes et non seulement les nouvelles autorisations.

---
[Source](https://thehackernews.com/2026/05/the-back-door-attackers-know-about-and.html){:target="_blank"}
