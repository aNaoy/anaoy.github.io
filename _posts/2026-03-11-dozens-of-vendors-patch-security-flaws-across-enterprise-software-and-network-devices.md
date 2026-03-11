---
title: 'Dozens of Vendors Patch Security Flaws Across Enterprise Software and Network Devices'
date: 2026-03-11
permalink: /posts/2026/03/11/dozens-of-vendors-patch-security-flaws-across-enterprise-software-and-network-devices/
tags:
- veille-cyber
- hackernews
---
### Vague de correctifs critiques dans l'écosystème logiciel et réseau

De nombreux éditeurs de logiciels et fournisseurs d'équipements réseau ont récemment publié des correctifs de sécurité pour combler des vulnérabilités critiques. Cette campagne de mise à jour touche des acteurs majeurs tels que SAP, Microsoft, Adobe et HPE.

**Points clés :**
* **SAP :** Correction de deux failles critiques permettant l'exécution de code arbitraire.
* **HPE :** Résolution d'une vulnérabilité majeure affectant l'interface de gestion des commutateurs Aruba.
* **Microsoft et Adobe :** Publication massive de correctifs pour un total combiné de 164 vulnérabilités (84 pour Microsoft, 80 pour Adobe).
* **Écosystème étendu :** Une longue liste d'autres fournisseurs (incluant Cisco, VMware, GitLab, Google et de nombreuses distributions Linux) a également diffusé des bulletins de sécurité.

**Vulnérabilités majeures :**
* **CVE-2019-17571 (Score CVSS 9.8) :** Injection de code dans SAP FS-QUO due à une version obsolète d'Apache Log4j 1.2.17.
* **CVE-2026-27685 (Score CVSS 9.1) :** Désérialisation non sécurisée dans SAP NetWeaver Enterprise Portal.
* **CVE-2026-23813 (Score CVSS 9.8) :** Contournement d'authentification sur les interfaces de gestion des équipements Aruba AOS-CX, permettant potentiellement une prise de contrôle totale.

**Recommandations :**
* **Application immédiate des correctifs :** Il est impératif d'installer les dernières mises à jour publiées par les éditeurs mentionnés pour limiter le risque d'exploitation.
* **Priorisation :** Les correctifs concernant les accès distants et l'administration réseau (comme pour Aruba ou SAP) doivent être traités en priorité absolue en raison de leur impact critique sur l'intégrité des systèmes.
* **Veille active :** Les administrateurs système sont invités à consulter régulièrement les portails de sécurité de leurs fournisseurs respectifs pour identifier les correctifs applicables à leur infrastructure.

---
[Source](https://thehackernews.com/2026/03/dozens-of-vendors-patch-security-flaws.html){:target="_blank"}
