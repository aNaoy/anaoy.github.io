---
title: 'SQLi flaw in Elementor Ally plugin impacts 250k+ WordPress sites'
date: 2026-03-11
permalink: /posts/2026/03/11/sqli-flaw-in-elementor-ally-plugin-impacts-250k-wordpress-sites/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilité SQLi critique dans le plugin WordPress "Ally"

Une faille d'injection SQL (SQLi) expose plus de 250 000 sites WordPress utilisant le plugin d'accessibilité "Ally" d'Elementor. Cette vulnérabilité permet à un attaquant non authentifié d'extraire des données sensibles de la base de données via des techniques d'injection à l'aveugle basées sur le temps.

**Points clés :**
* **Vulnérabilité :** Injection SQL (SQLi) due à une mauvaise gestion des paramètres URL dans la méthode `get_global_remediations()`.
* **Conditions d'exploitation :** Le plugin doit être connecté à un compte Elementor et le module "Remediation" doit être activé.
* **Impact :** Lecture, modification ou suppression d'informations dans la base de données sans authentification.
* **CVE :** CVE-2026-2313.
* **Versions affectées :** Toutes les versions jusqu'à la 4.0.3.

**Recommandations :**
* **Mise à jour immédiate :** Passer impérativement à la version 4.1.0 du plugin Ally.
* **Maintenance système :** Mettre à jour WordPress vers la version 6.9.2 pour corriger dix autres vulnérabilités critiques (XSS, SSRF, contournement d'autorisation).

---
[Source](https://www.bleepingcomputer.com/news/security/sqli-flaw-in-elementor-ally-plugin-impacts-250k-plus-wordpress-sites/){:target="_blank"}
