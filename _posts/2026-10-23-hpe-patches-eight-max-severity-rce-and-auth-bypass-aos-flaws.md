---
title: 'HPE patches eight max severity RCE and auth bypass AOS flaws'
date: 2026-10-23
permalink: /posts/2026/10/23/hpe-patches-eight-max-severity-rce-and-auth-bypass-aos-flaws/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilités critiques dans ArubaOS : HPE publie des correctifs urgents

HPE a déployé des mises à jour de sécurité pour corriger 72 vulnérabilités au sein d'ArubaOS, le système d'exploitation équipant ses infrastructures réseau (points d'accès, contrôleurs et passerelles). Parmi ces failles, huit présentent un niveau de sévérité maximal et permettent à des attaquants distants non authentifiés d'exécuter du code arbitraire ou de contourner les mécanismes d'authentification sans interaction utilisateur.

**Points clés :**
* **Impact :** Les versions AOS-8 et AOS-10 sont concernées.
* **Risque :** Attaques de faible complexité ne nécessitant aucun privilège initial.
* **État actuel :** Aucune preuve d'exploitation active ("in the wild") n'a été identifiée pour le moment.

**Vulnérabilités majeures (CVE) :**
* **CVE-2026-79844 :** Contournement d'authentification menant à une exécution de code (RCE) sur AOS-10.
* **CVE-2026-79845 :** Contournement d'authentification via le protocole PAPI sur AOS-10.
* **CVE-2026-79846 :** Injection de commande sans authentification sur AOS-8.
* **CVE-2026-79847 :** Dépassement de tampon (buffer overflow) sans authentification menant à une RCE sur AOS-10.
* **CVE-2026-79848 & CVE-2026-79849 :** Injections SQL sans authentification menant à une RCE sur AOS-8.
* **CVE-2026-79850 :** Contournement d'authentification menant à une RCE sur AOS-8.
* **CVE-2026-79851 :** Dépassement de tampon sans authentification menant à une RCE sur AOS-10.

**Recommandations :**
* **Mise à jour immédiate :** Installer les correctifs fournis par HPE sans délai.
* **Segmentation réseau :** Restreindre l'accès aux interfaces de gestion (CLI et Web) à un segment réseau dédié (VLAN) ou isoler ces accès via des politiques de pare-feu (L3 et supérieur).
* **Monitoring :** Mettre en place des contrôles d'audit et la journalisation des activités pour surveiller l'utilisation des ressources et les accès aux interfaces.

---
[Source](https://www.bleepingcomputer.com/news/security/hpe-patches-eight-max-severity-rce-and-auth-bypass-aos-flaws/){:target="_blank"}
