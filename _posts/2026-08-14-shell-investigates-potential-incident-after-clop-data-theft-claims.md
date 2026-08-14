---
title: 'Shell investigates potential incident after Clop data theft claims'
date: 2026-08-14
permalink: /posts/2026/08/14/shell-investigates-potential-incident-after-clop-data-theft-claims/
tags:
- veille-cyber
- bleepingcomp
---
### Cyberattaque par rançongiciel : Shell parmi les victimes du groupe Clop

Shell fait l'objet d'une enquête suite aux affirmations du groupe de rançongiciel Clop, qui prétend avoir dérobé 89 Go de données internes, incluant des plans d'ingénierie et des rapports techniques. Cette intrusion s'inscrit dans une campagne d'envergure visant des entreprises mondiales majeures (dont General Electric et Philips) via l'exploitation de logiciels PLM (Product Lifecycle Management).

**Points clés :**
* **Vecteur d'attaque :** Exploitation d'instances exposées sur Internet des solutions PTC Windchill et FlexPLM.
* **Mode opératoire :** Les attaquants déploient des *webshells* JSP pour exfiltrer des données sensibles liées aux cycles de vie des produits industriels.
* **Impact :** La campagne touche de nombreux secteurs critiques (aérospatial, défense, automobile, médical).

**Vulnérabilité identifiée :**
* **CVE-2026-12569 :** Faille critique de validation d'entrée (*improper input validation*) permettant l'exécution de code à distance (RCE). Cette vulnérabilité est activement exploitée et figure au catalogue des vulnérabilités connues (KEV) de la CISA.

**Recommandations :**
* **Application des correctifs :** Déployer immédiatement les patchs de sécurité fournis par PTC (disponibles depuis le 17 juin 2026).
* **Audit de sécurité :** Examiner les environnements PTC Windchill et FlexPLM à la recherche d'indicateurs de compromission (IOC) et de *webshells* suspects.
* **Veille réglementaire :** Les autorités de cybersécurité (dont la CISA et le BSI allemand) recommandent une sécurisation urgente des instances exposées pour contrer cette menace active.

---
[Source](https://www.bleepingcomputer.com/news/security/shell-investigates-potential-incident-after-clop-data-theft-claims/){:target="_blank"}
