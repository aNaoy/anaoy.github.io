---
title: 'Over 10,000 Zimbra servers vulnerable to ongoing XSS attacks'
date: 2026-04-24
permalink: /posts/2026/04/24/over-10000-zimbra-servers-vulnerable-to-ongoing-xss-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilité majeure sur les serveurs Zimbra : plus de 10 000 instances exposées

Plus de 10 500 serveurs Zimbra Collaboration Suite (ZCS) restent vulnérables à des attaques de type Cross-Site Scripting (XSS) activement exploitées. La CISA a ajouté cette faille à son catalogue des vulnérabilités connues (KEV) et impose aux agences fédérales américaines une remédiation urgente.

**Points clés :**
* **Menace active :** Les attaquants exploitent la vulnérabilité sans aucune interaction de l'utilisateur, simplement en envoyant un e-mail malveillant visualisé via l'interface web (Classic UI) de Zimbra.
* **Ciblage stratégique :** Les serveurs Zimbra sont des cibles récurrentes pour des groupes APT (tels qu'APT28) visant des agences gouvernementales et des infrastructures critiques.
* **Répartition géographique :** La majorité des serveurs non corrigés se situent en Asie et en Europe.

**Vulnérabilités :**
* **CVE-2025-48700 :** Faille XSS critique permettant l'exécution de JavaScript arbitraire dans la session de l'utilisateur, entraînant potentiellement le vol d'informations sensibles. Affecte les versions ZCS 8.8.15, 9.0, 10.0 et 10.1.
* **CVE-2025-66376 :** Autre vulnérabilité XSS précédemment utilisée dans des campagnes d'espionnage contre des entités gouvernementales.

**Recommandations :**
* **Mise à jour immédiate :** Appliquer sans délai les correctifs de sécurité fournis par Synacor (disponibles depuis juin 2025).
* **Audit d'exposition :** Vérifier l'état de mise à jour de toutes les instances Zimbra exposées sur Internet.
* **Surveillance :** Surveiller les logs de messagerie pour détecter toute activité suspecte ou exécution de scripts inhabituels dans les sessions utilisateurs.

---
[Source](https://www.bleepingcomputer.com/news/security/cisa-says-zimbra-flaw-now-exploited-over-10k-servers-vulnerable/){:target="_blank"}
