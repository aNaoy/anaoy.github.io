---
title: 'HTTP Requests with X-Vercel-Set-Bypass-Cookie Header, (Tue, Apr 28th)'
date: 2026-04-28
permalink: /posts/2026/04/28/http-requests-with-x-vercel-set-bypass-cookie-header-tue-apr-28th/
tags:
- veille-cyber
- sans-isc
---
### Analyse des requêtes suspectes avec l'en-tête X-Vercel-Set-Bypass-Cookie

Des requêtes malveillantes exploitant l'en-tête `X-Vercel-Set-Bypass-Cookie` ont été détectées sur des serveurs honeypot. Cette tentative semble viser le contournement des mécanismes de protection de déploiement de la plateforme Vercel.

**Points clés :**
* **Fonctionnement légitime :** Vercel utilise un en-tête nommé `x-vercel-protection-bypass` (géré par un secret configuré par l'utilisateur) pour désactiver temporairement les pare-feu d'applications web (WAF) durant les tests ou les pipelines CI/CD.
* **Comportement suspect :** L'utilisation de `X-Vercel-Set-Bypass-Cookie` permet au serveur de définir un cookie persistant pour maintenir ce contournement via un navigateur.
* **Anomalie détectée :** L'attaquant a utilisé une valeur non documentée (`samesite-none-secure`) dans l'en-tête, suggérant une tentative d'exploration de vulnérabilités ou de vol d'informations via la manipulation de cookies.
* **Méthodologie :** Les attaques observées transitent par des proxys ouverts, indiquant une volonté de dissimuler l'origine réelle de l'exploitation.

**Vulnérabilités :**
* Aucune CVE spécifique n'est associée à ce jour, car il s'agit d'une observation de reconnaissance active plutôt que d'une vulnérabilité logicielle confirmée. Le risque principal réside dans une configuration permissive des protections Vercel.

**Recommandations :**
* **Audit des configurations :** Vérifiez si la fonctionnalité de contournement de protection (`x-vercel-protection-bypass`) est activée sur vos déploiements et assurez-vous que les secrets associés ne sont pas exposés ou devinables.
* **Surveillance des logs :** Surveillez vos logs d'accès à la recherche de l'en-tête `X-Vercel-Set-Bypass-Cookie` ou d'autres tentatives d'injection d'en-têtes de contournement.
* **Principe du moindre privilège :** Désactivez systématiquement tout mécanisme de contournement de sécurité sur les environnements de production.

---
[Source](https://isc.sans.edu/diary/rss/32930){:target="_blank"}
