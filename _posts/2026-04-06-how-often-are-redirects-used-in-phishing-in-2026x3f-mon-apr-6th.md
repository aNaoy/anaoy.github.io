---
title: 'How often are redirects used in phishing in 2026&#x3f;, (Mon, Apr 6th)'
date: 2026-04-06
permalink: /posts/2026/04/06/how-often-are-redirects-used-in-phishing-in-2026x3f-mon-apr-6th/
tags:
- veille-cyber
- sans-isc
---
### L’omniprésence des redirections dans les campagnes de phishing

Bien que souvent considérée comme une vulnérabilité mineure, la redirection ouverte (*open redirect*) demeure un vecteur privilégié par les attaquants pour contourner les mécanismes de filtrage et gagner la confiance des utilisateurs. L'analyse des emails de phishing au premier trimestre 2026 révèle que plus de 21 % d'entre eux exploitent des mécanismes de redirection pour masquer la destination finale malveillante derrière des domaines légitimes et réputés (Google, Bing, etc.).

**Points clés :**
*   **Contournement de la sécurité :** Les liens utilisant des redirections vers des sites de confiance échappent aux filtres anti-spam et aux analyses heuristiques.
*   **Variété des mécanismes :** L'usage ne se limite pas aux redirections "ouvertes" classiques. Les attaquants détournent également des fonctionnalités de tracking, des pages de déconnexion, des raccourcisseurs d'URL et des redirections dites "semi-ouvertes" (nécessitant des jetons réutilisables à longue durée de vie).
*   **Persistance :** Malgré l'absence de cette vulnérabilité dans le top 10 de l'OWASP, les tentatives d'identification de points de terminaison vulnérables sur les serveurs sont constantes.

**Vulnérabilités :**
*   **Open Redirect (CWE-601) :** Bien que non cataloguée sous une CVE spécifique unique, cette classe de vulnérabilité permet à un attaquant d'utiliser une application légitime pour rediriger des utilisateurs vers un site malveillant.

**Recommandations :**
*   **Audit des points de terminaison :** Identifier et supprimer les points de redirection inutiles au sein des applications métier.
*   **Restriction d'accès :** Si une fonctionnalité de redirection est indispensable, restreindre les destinations autorisées via une liste blanche (*allowlist*) de domaines de confiance.
*   **Monitoring :** Surveiller les logs des serveurs à la recherche de schémas d'utilisation anormaux liés aux mécanismes de redirection.
*   **Gestion des jetons :** Pour les redirections utilisant des jetons, limiter leur durée de vie et, si possible, les lier à une session utilisateur ou une adresse IP spécifique pour éviter leur réutilisation abusive.

---
[Source](https://isc.sans.edu/diary/rss/32870){:target="_blank"}
