---
title: 'Broken Phishing URLs, (Thu, Feb 5th)'
date: 2026-02-05
permalink: /posts/2026/02/05/broken-phishing-urls-thu-feb-5th/
tags:
- veille-cyber
- sans-isc
---
**URL de Phishing Dégradées : Une Technique de Contournement des Défenses**

Des campagnes de phishing récentes utilisent des URL dont le format est intentionnellement dégradé. Au lieu de suivre la structure standard "nom=valeur" pour les paramètres, ces URL incluent des caractères invalides après le signe "&" (par exemple, "&*(Df").

Les navigateurs web ignorent généralement ces paramètres malformés, permettant ainsi à l'utilisateur d'accéder au site web malveillant sans erreur apparente. Cette technique vise à contourner les mécanismes de sécurité qui reposent sur l'analyse syntaxique des URL, tels que les expressions régulières (regex), les routines de normalisation d'URL ou les outils d'extraction d'indicateurs de compromission (IOC).

**Points Clés :**

*   Utilisation d'URL avec des paramètres malformés pour déjouer les contrôles de sécurité.
*   Les navigateurs web traitent ces URL en ignorant les parties invalides.
*   Les attaquants cherchent à perturber les processus d'analyse automatique des URL par les systèmes de sécurité.

**Vulnérabilités :**

Aucune vulnérabilité spécifique avec un identifiant CVE n'est mentionnée dans l'article. La technique cible plutôt la manière dont les systèmes de sécurité analysent et interprètent les URL.

**Recommandations :**

*   Mettre en place des règles de détection basées sur des expressions régulières (regex) qui puissent identifier les URL avec des paramètres malformés ou non conformes.
*   Affiner les routines de normalisation d'URL pour qu'elles gèrent correctement les caractères invalides et puissent signaler les URL suspectes.
*   Développer ou adapter des outils d'extraction d'IOC pour qu'ils soient capables de traiter ces variations d'URL.
*   Sensibiliser les utilisateurs aux signes de phishing, même si les liens semblent légitimes au premier abord.

---
[Source](https://isc.sans.edu/diary/rss/32686){:target="_blank"}
