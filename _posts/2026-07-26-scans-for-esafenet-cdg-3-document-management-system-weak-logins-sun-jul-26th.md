---
title: 'Scans for ESAFENET CDG 3 Document Management System Weak Logins, (Sun, Jul 26th)'
date: 2026-07-26
permalink: /posts/2026/07/26/scans-for-esafenet-cdg-3-document-management-system-weak-logins-sun-jul-26th/
tags:
- veille-cyber
- sans-isc
---
### Campagne d'exploitation des accès par défaut sur ESAFENET CDG

Des campagnes de scans automatisés ciblent actuellement le système de gestion de documents ESAFENET CDG (Content Data Guard) en exploitant des identifiants de connexion par défaut largement documentés. Malgré la complexité apparente du mot de passe par défaut (ex: `Est@Spc820`), sa nature publique facilite les compromissions.

**Points clés :**
* Le produit, principalement utilisé sur le marché chinois, est vulnérable à des failles classiques telles que l'injection SQL, le XSS et l'utilisation de mots de passe par défaut.
* Des modèles d'automatisation (Nuclei templates) incluant ces identifiants sont disponibles publiquement depuis 2023, permettant à des acteurs malveillants de scanner massivement les instances exposées.

**Vulnérabilités :**
* **Mots de passe par défaut :** Utilisation d'identifiants pré-configurés connus (`secadmin` / `Est@Spc820`).
* **Autres failles connues :** Injection SQL et Cross-Site Scripting (XSS).

**Recommandations :**
* **Changement immédiat :** Modifier impérativement tous les mots de passe par défaut lors de l'installation et privilégier des mots de passe uniques et robustes.
* **Réduction de la surface d'attaque :** Restreindre l'accès à l'interface d'administration de CDG en ne l'exposant pas directement sur Internet (utilisation d'un VPN ou d'un accès réseau filtré).
* **Veille et maintenance :** Appliquer régulièrement les correctifs de sécurité fournis par l'éditeur pour pallier les vulnérabilités de type injection SQL et XSS.

---
[Source](https://isc.sans.edu/diary/rss/33184){:target="_blank"}
