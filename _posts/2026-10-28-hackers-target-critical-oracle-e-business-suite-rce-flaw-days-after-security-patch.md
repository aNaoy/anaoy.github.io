---
title: 'Hackers Target Critical Oracle E-Business Suite RCE Flaw Days After Security Patch'
date: 2026-10-28
permalink: /posts/2026/10/28/hackers-target-critical-oracle-e-business-suite-rce-flaw-days-after-security-patch/
tags:
- veille-cyber
- hackernews
---
### Exploitation active de la faille critique dans Oracle E-Business Suite

Des cyberattaquants exploitent activement une vulnérabilité critique récemment corrigée dans Oracle E-Business Suite (EBS), quelques jours seulement après la publication du correctif par l'éditeur.

**Points clés**
* **Nature de l'attaque :** La vulnérabilité permet une injection SQL non authentifiée via le servlet *Thin Client Framework* (TCF), pouvant être enchaînée pour obtenir une exécution de code à distance (RCE).
* **Impact :** Un attaquant peut exécuter des requêtes SQL avec les privilèges de l'utilisateur `APPS` et compromettre l'hôte applicatif en exécutant des commandes système. Les données sensibles (RH, paie, finances) sont directement exposées.
* **Vecteur :** Les déploiements exposés sur Internet sont les plus vulnérables, mais les réseaux internes sont également menacés en cas de compromission d'un segment adjacent.

**Vulnérabilité**
* **CVE-2026-101767 :** Score CVSS de 9.8. Il s'agit d'un défaut d'authentification dans la bibliothèque d'objets Oracle Application.

**Recommandations**
* **Mise à jour :** Appliquer immédiatement le dernier *Critical Patch Update* fourni par Oracle.
* **Mesures d'atténuation temporaires :**
    * Retirer `/OA_HTML/AppsTCFServer` de la liste d'autorisation du pare-feu applicatif.
    * Restreindre l'accès à la couche Web d'EBS aux seuls réseaux de confiance.
* **Surveillance :** Surveiller les requêtes POST non authentifiées vers le servlet TCF et vérifier la présence de fichiers suspects dans `$APPLPTMP` ou l'exécution inattendue de `/bin/sh` par le compte Oracle.

---
[Source](https://thehackernews.com/2026/10/hackers-target-critical-oracle-e.html){:target="_blank"}
