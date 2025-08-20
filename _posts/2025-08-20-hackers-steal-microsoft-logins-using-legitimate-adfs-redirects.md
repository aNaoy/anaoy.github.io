---
title: 'Hackers steal Microsoft logins using legitimate ADFS redirects'
date: 2025-08-20
permalink: /posts/2025/08/20/hackers-steal-microsoft-logins-using-legitimate-adfs-redirects/
tags:
- veille-cyber
- bleepingcomp
---
### L'astuce ADFS détourne les utilisateurs vers le phishing Microsoft 365

Des cybercriminels exploitent désormais une méthode sophistiquée pour dérober des identifiants Microsoft 365. Elle consiste à utiliser des liens légitimes d'Office.com qui redirigent vers des pages de phishing, contournant ainsi les défenses classiques et l'authentification multi-facteurs.

L'attaque commence souvent par un clic sur un lien sponsorisé malveillant dans les résultats de recherche Google visant Office 365. Ce lien redirige d'abord vers un domaine Microsoft approuvé, puis vers un site tiers contrôlé par l'attaquant, avant d'acheminer l'utilisateur vers la page de phishing finale.

Le cœur de cette technique réside dans l'utilisation de services Active Directory Federation Services (ADFS) configurés sur un tenant Microsoft personnalisé par l'attaquant. L'ADFS, utilisé pour l'authentification unique, permet au domaine de phishing d'être autorisé par l'infrastructure Microsoft, le rendant invisible pour l'utilisateur final pendant le processus de redirection. Pour éviter la détection automatisée, le site tiers est rempli de contenu légitime apparent, et des restrictions conditionnelles limitent l'accès à la page de phishing uniquement aux cibles jugées valides.

Cette campagne semble relever de l'expérimentation de nouvelles méthodes d'attaque par un acteur malveillant cherchant à exploiter la confiance accordée aux liens Microsoft.

**Points Clés :**

*   Utilisation de liens légitimes Microsoft Office.com.
*   Exploitation de l'Active Directory Federation Services (ADFS).
*   Contournement des détections basées sur les URL et de l'authentification multi-facteurs.
*   Redirections multiples impliquant un domaine tiers contrôlé par l'attaquant.
*   Mise en place de conditions pour restreindre l'accès à la page de phishing.

**Vulnérabilités :**

Aucune vulnérabilité spécifique (avec CVE) n'est explicitement mentionnée dans l'article. La technique exploite plutôt la confiance accordée à l'infrastructure légitime de Microsoft et la configuration d'ADFS.

**Recommandations :**

*   Surveiller les redirections ADFS vers des emplacements malveillants.
*   Vérifier les paramètres des publicités dans les redirections Google vers Office.com pour identifier des domaines ou redirections suspects.

---
[Source](https://www.bleepingcomputer.com/news/security/hackers-steal-microsoft-logins-using-legitimate-adfs-redirects/){:target="_blank"}
