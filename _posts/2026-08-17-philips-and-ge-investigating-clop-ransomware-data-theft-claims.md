---
title: 'Philips and GE investigating Clop ransomware data theft claims'
date: 2026-08-17
permalink: /posts/2026/08/17/philips-and-ge-investigating-clop-ransomware-data-theft-claims/
tags:
- veille-cyber
- bleepingcomp
---
### Vague de cyberattaques du groupe Clop contre les plateformes PTC

Le groupe de cybercriminels Clop a revendiqué le vol de données sensibles appartenant à plusieurs entreprises majeures, dont General Electric, Philips et Shell. Ces intrusions s'inscrivent dans une campagne de grande ampleur ciblant les serveurs exposés à Internet utilisant les logiciels PTC Windchill et FlexPLM.

**Points clés :**
* **Cible :** Plus de 40 entreprises, dont des géants de l'aérospatiale, de l'automobile et de la technologie.
* **Méthode :** Exploitation d'une vulnérabilité critique pour déployer des webshells JSP, permettant l'exfiltration de données (plans, diagrammes, sauvegardes, documents confidentiels).
* **Contexte :** Le groupe Clop est un acteur récidiviste spécialisé dans l'extorsion de données via des failles « zero-day » sur des logiciels d'entreprise (MOVEit, Oracle EBS, etc.).

**Vulnérabilités :**
* **CVE-2026-12569 :** Une faille critique de validation d'entrée défectueuse (improper input validation) dans PTC Windchill et PTC FlexPLM, actuellement exploitée activement par des attaquants et classée au catalogue des vulnérabilités connues (KEV) par la CISA.

**Recommandations :**
* **Application de correctifs :** PTC a publié des correctifs dès le 17 juin ; leur déploiement immédiat est impératif.
* **Audit de sécurité :** Rechercher les indicateurs de compromission (IOC) sur les instances PTC Windchill et FlexPLM exposées.
* **Action d'urgence :** Les autorités de cybersécurité (notamment la CISA et le BSI allemand) exigent une sécurisation rapide de ces instances, considérant le risque élevé d'exfiltration de données sensibles.

---
[Source](https://www.bleepingcomputer.com/news/security/philips-and-ge-investigating-clop-ransomware-data-theft-claims/){:target="_blank"}
