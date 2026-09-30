---
title: 'Microsoft to block Entra ID script injection attacks starting October'
date: 2026-09-30
permalink: /posts/2026/09/30/microsoft-to-block-entra-id-script-injection-attacks-starting-october/
tags:
- veille-cyber
- bleepingcomp
---
### Renforcement de la sécurité des connexions Microsoft Entra ID contre l'injection de scripts

Dès la mi-octobre 2026, Microsoft déploiera une nouvelle politique de sécurité du contenu (Content Security Policy - CSP) pour renforcer la protection des pages de connexion de Microsoft Entra ID. Cette mise à jour limitera l'exécution de scripts exclusivement aux domaines approuvés du réseau de diffusion de contenu (CDN) de Microsoft, bloquant ainsi tout code externe non autorisé.

**Points clés :**
* **Objectif :** Prévenir les attaques par injection de scripts sur les pages d'authentification (`login.microsoftonline.com`).
* **Portée :** La mesure s'applique uniquement aux connexions via navigateur. Les flux d'authentification basés sur MSAL (Microsoft Authentication Library) et les API ne sont pas concernés.
* **Déploiement :** Automatique et activé par défaut pour tous les clients, sans nécessiter de configuration spécifique.

**Vulnérabilités adressées :**
* **Cross-Site Scripting (XSS) :** Cette mesure vise à contrer l'injection de code malveillant sur les pages de connexion, une technique souvent utilisée pour le vol d'identifiants.

**Recommandations pour les administrateurs :**
* **Inventaire des outils :** Identifier et cesser l'utilisation d'extensions de navigateur ou d'outils tiers qui injectent des scripts ou du code dans les pages de connexion.
* **Tests de compatibilité :** Tester les flux de connexion avant l'échéance d'octobre pour détecter d'éventuels dysfonctionnements liés à ces outils.
* **Surveillance :** Consulter la console de développement du navigateur lors des sessions de test pour identifier les violations de politique CSP (affichées en rouge) afin de corriger les dépendances non conformes.

---
[Source](https://www.bleepingcomputer.com/news/security/microsoft-to-block-entra-id-script-injection-attacks-starting-october/){:target="_blank"}
