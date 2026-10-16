---
title: 'Zero-click attacks used targeted ads to deliver Candiru spyware'
date: 2026-10-16
permalink: /posts/2026/10/16/zero-click-attacks-used-targeted-ads-to-deliver-candiru-spyware/
tags:
- veille-cyber
- bleepingcomp
---
### AdFection : Le spyware Candiru propagé via des publicités ciblées

Des chercheurs de Citizen Lab ont mis en lumière une campagne d'espionnage sophistiquée baptisée « AdFection ». Cette attaque de type *zero-click* permet d'infecter des appareils avec le spyware Candiru simplement en affichant une publicité malveillante, sans aucune interaction de l'utilisateur.

**Points clés**
* **Vecteur d'attaque :** La société Discover-Tech exploite l'écosystème publicitaire légitime pour diffuser des publicités contenant du code JavaScript malveillant.
* **Ciblage chirurgical :** Via sa plateforme *Controlium*, l'attaquant analyse l'adresse IP et les identifiants de l'appareil avant de décider s'il déploie la charge utile. Cela permet de rester furtif en ne visant que des cibles spécifiques.
* **Ampleur :** Entre mars et juin 2026, la campagne a participé à des centaines de millions d'enchères publicitaires sur plus de 75 000 applications et 120 000 sites web, exposant potentiellement des millions d'utilisateurs.
* **Impact :** Des preuves confirment l'infection d'au moins 45 appareils appartenant à des employés d'Al Jazeera. Le logiciel malveillant, identifié comme étant lié à Candiru (connu pour son outil *DevilsTongue*), est capable de dérober des fichiers, des identifiants et des messages.

**Vulnérabilités**
* Bien que l'article souligne l'exploitation de failles *zero-day* par Candiru par le passé, la méthode « AdFection » repose sur une exploitation silencieuse du rendu publicitaire via des scripts malveillants injectés dans les réseaux d'annonces. Aucune CVE spécifique n'est mentionnée pour cette technique, le succès de l'attaque reposant sur l'abus des mécanismes publicitaires standards.

**Recommandations**
* **Réaction de l'écosystème :** Les principaux réseaux publicitaires (Google, IAB Europe, Beeswax, etc.) ont été notifiés et ont procédé au blocage des comptes et domaines associés à Discover-Tech.
* **Protection des utilisateurs :**
    * Utiliser des bloqueurs de publicités (*ad-blockers*) réputés pour empêcher le chargement de scripts publicitaires tiers.
    * Maintenir les navigateurs et le système d'exploitation à jour pour limiter les risques liés aux exploits *zero-day* que le spyware pourrait tenter d'utiliser en complément.
    * Privilégier une navigation sécurisée et limiter l'exposition sur des sites non essentiels.

---
[Source](https://www.bleepingcomputer.com/news/security/zero-click-attacks-used-targeted-ads-to-deliver-candiru-spyware/){:target="_blank"}
