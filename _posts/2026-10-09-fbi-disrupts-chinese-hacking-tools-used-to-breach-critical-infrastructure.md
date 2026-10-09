---
title: 'FBI disrupts Chinese hacking tools used to breach critical infrastructure'
date: 2026-10-09
permalink: /posts/2026/10/09/fbi-disrupts-chinese-hacking-tools-used-to-breach-critical-infrastructure/
tags:
- veille-cyber
- bleepingcomp
---
### Démantèlement de l'infrastructure cybercriminelle du groupe Flax Typhoon

Le FBI a saisi sept domaines utilisés par le groupe chinois Flax Typhoon et la société Integrity Technology Group pour piloter deux plateformes de cyberattaques : **MicroScan** (scan de vulnérabilités) et **FishHub** (hameçonnage et exfiltration de données). Ces outils ont permis de cibler des infrastructures critiques (énergie, aéroports, éducation) à travers le monde.

**Points clés :**
* **Collaboration étatique :** Integrity Tech, sous contrat avec le gouvernement chinois, a développé des outils exploitant des botnets (notamment Mirai) pour automatiser les intrusions.
* **Mode opératoire :** Utilisation de scripts de scan automatisés, attaques par pulvérisation de mots de passe (EBurst) sur Microsoft Exchange, et installation de VPN SoftEther pour maintenir un accès persistant.
* **Impact :** Des données provenant de plus de 20 organisations, incluant des universités et des agences gouvernementales, ont été exfiltrées.

**Vulnérabilités exploitées :**
Les attaquants ciblaient activement des failles connues dans des logiciels largement déployés :
* **CVE-2015-3306** (ProFTPD)
* **CVE-2015-5477** (ISC BIND)
* **CVE-2016-3081** (Apache Struts)
* **CVE-2021-3199** (ONLYOFFICE)
* **CVE-2023-22894** (Strapi)
* **CVE-2014-6278** (Shellshock / Bash)
* **CVE-2019-11510** (Pulse Secure)
* **CVE-2021-22205** (GitLab)

**Recommandations :**
* **Gestion des correctifs :** Appliquer immédiatement les patchs de sécurité pour les vulnérabilités listées ci-dessus.
* **Durcissement du réseau :** Désactiver tous les services exposés non nécessaires.
* **Contrôle d'accès :** Renforcer l'authentification par l'usage obligatoire du MFA (Multi-Factor Authentication).
* **Veille :** Consulter l'avis de sécurité conjoint émis par le FBI, la CISA et la NSA pour intégrer les indicateurs de compromission (IoC) fournis dans les outils de détection.

---
[Source](https://www.bleepingcomputer.com/news/security/fbi-disrupts-chinese-hacking-tools-used-to-breach-critical-infrastructure/){:target="_blank"}
