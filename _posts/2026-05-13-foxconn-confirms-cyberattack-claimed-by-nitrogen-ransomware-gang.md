---
title: 'Foxconn confirms cyberattack claimed by Nitrogen ransomware gang'
date: 2026-05-13
permalink: /posts/2026/05/13/foxconn-confirms-cyberattack-claimed-by-nitrogen-ransomware-gang/
tags:
- veille-cyber
- bleepingcomp
---
### Cyberattaque par ransomware contre les sites nord-américains de Foxconn

Le géant de l'électronique Foxconn a confirmé avoir subi une cyberattaque touchant plusieurs de ses usines en Amérique du Nord. Le groupe de cybercriminels « Nitrogen » a revendiqué cette intrusion, affirmant avoir exfiltré 8 To de données contenant environ 11 millions de documents confidentiels, incluant des projets et des plans techniques appartenant à des clients majeurs tels qu'Apple, Nvidia, Google, Intel et AMD.

**Points clés :**
* **Nature de l'attaque :** Utilisation du ransomware « Nitrogen », un logiciel malveillant initialement lié au groupe BlackCat/ALPHV et s'appuyant désormais sur le code source ayant fuité du ransomware Conti.
* **Impact opérationnel :** Foxconn a activé ses protocoles de réponse aux incidents pour assurer la continuité de la production. Les usines concernées sont actuellement en phase de reprise d'activité.
* **Antécédents :** Foxconn est une cible récurrente, ayant déjà été visé par les groupes LockBit (2024), DoppelPaymer (2020) et d'autres incidents en 2022.

**Vulnérabilités :**
* Bien qu'aucune CVE spécifique n'ait été associée à cette intrusion, le groupe Nitrogen est connu pour exploiter des failles via des campagnes publicitaires malveillantes (malvertising). À noter que le malware utilisé par Nitrogen présente une erreur de conception (bug dans le chiffrement ESXi) qui peut corrompre irrémédiablement les données.

**Recommandations :**
* **Renforcement de la surveillance :** Détecter les accès non autorisés aux infrastructures critiques via des solutions EDR/XDR robustes.
* **Gestion des sauvegardes :** Maintenir des sauvegardes immuables et déconnectées du réseau principal pour éviter la destruction des données en cas d'attaque par chiffrement.
* **Sensibilisation et filtrage :** Bloquer les vecteurs d'entrée courants (publicités malveillantes, phishing) et restreindre les accès aux serveurs ESXi ou aux environnements de virtualisation sensibles.
* **Analyse de la surface d'exposition :** Auditer régulièrement les accès distants et les actifs exposés sur Internet, en particulier pour les grandes entreprises industrielles ayant des chaînes d'approvisionnement critiques.

---
[Source](https://www.bleepingcomputer.com/news/security/electronics-giant-foxconn-confirms-cyberattack-on-north-american-factories/){:target="_blank"}
