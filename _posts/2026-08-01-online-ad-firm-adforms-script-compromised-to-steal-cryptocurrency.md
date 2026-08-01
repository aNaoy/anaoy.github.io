---
title: 'Online ad firm Adform’s script compromised to steal cryptocurrency'
date: 2026-08-01
permalink: /posts/2026/08/01/online-ad-firm-adforms-script-compromised-to-steal-cryptocurrency/
tags:
- veille-cyber
- bleepingcomp
---
### Attaque par chaîne d'approvisionnement via la plateforme publicitaire Adform

La société Adform, acteur majeur du secteur de l'adtech, a été victime d'une attaque par chaîne d'approvisionnement ayant conduit à l'injection de code malveillant dans son script de suivi `trackpoint-async.js`. Ce script, intégré sur de nombreux sites web, a été détourné pour dérober des cryptomonnaies.

**Points clés :**
* **Fonctionnement :** Le script malveillant surveillait le presse-papier des visiteurs et remplaçait automatiquement les adresses de portefeuilles (Bitcoin, Ethereum, TRON) par celles des attaquants. Il pouvait également modifier les adresses affichées directement sur les pages web.
* **Exfiltration :** Des données (adresse IP, site référent, URL) étaient envoyées vers un serveur distant contrôlé par les assaillants (84.32.102[.]230:7744).
* **Détection :** La compromission, active pendant environ une semaine, n'a été détectée par aucun moteur antivirus sur VirusTotal.
* **Statut actuel :** Le code malveillant a été retiré par Adform. L'entreprise précise qu'il ne s'agissait pas d'un logiciel persistant, mais d'une exécution active uniquement pendant la consultation des pages affectées.

**Vulnérabilités :**
* Aucune CVE n'a été associée à cet incident, l'attaque reposant sur l'injection directe de code (trojanisation) dans le script légitime de l'infrastructure de la victime.

**Recommandations :**
* **Pour les utilisateurs finaux :** Vider les cookies et le cache du navigateur pour éliminer toute trace résiduelle du script malveillant.
* **Pour les administrateurs de sites web :** Bien que le code ait été retiré par Adform, une vigilance accrue est recommandée lors de l'intégration de scripts tiers. L'implémentation de politiques de sécurité de contenu (CSP - Content Security Policy) strictes peut limiter l'impact de ce type d'attaques en empêchant l'exécution de scripts provenant de sources non autorisées ou la communication avec des domaines suspects.

---
[Source](https://www.bleepingcomputer.com/news/security/online-ad-firm-adforms-script-compromised-to-steal-cryptocurrency/){:target="_blank"}
