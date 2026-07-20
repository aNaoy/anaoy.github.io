---
title: 'Multiples vulnérabilités dans WordPress (20 juillet 2026)'
date: 2026-07-20
permalink: /posts/2026/07/20/multiples-vulnerabilites-dans-wordpress-20-juillet-2026/
tags:
- veille-cyber
- certfr
---
### Vulnérabilités critiques dans WordPress : Risque d'exécution de code à distance

Plusieurs versions de WordPress sont exposées à des vulnérabilités critiques pouvant permettre à un attaquant non authentifié d'exécuter du code arbitraire à distance (RCE) en combinant deux failles. Le CERT-FR alerte sur l'existence d'une preuve de concept (PoC) publique et prévoit des tentatives d'exploitation massive.

**Systèmes affectés :**
* WordPress 6.8.x (antérieures à 6.8.6)
* WordPress 6.9.x (antérieures à 6.9.5)
* WordPress 7.x (antérieures à 7.0.2)
* WordPress 7.1.x (antérieures à 7.1 beta2)

**Vulnérabilités identifiées :**
* **CVE-2026-60137 :** Injection SQL (SQLi).
* **CVE-2026-63030 :** Contournement de la politique de sécurité.
* *Note :* L'exploitation conjointe de ces deux failles sur les versions 6.9 et ultérieures permet l'exécution de code arbitraire à distance.

**Recommandations :**
* **Priorité absolue :** Appliquer les correctifs officiels fournis par WordPress sans délai.
* **Mesure de contournement (si la mise à jour est différée) :** Bloquer l'accès non authentifié à l'API REST de WordPress via un pare-feu applicatif (WAF). Il est spécifiquement recommandé de bloquer les requêtes ciblant le chemin `/wp-json/batch/v1` contenant le paramètre `rest_route=/batch/v1`.

---
[Source](https://www.cert.ssi.gouv.fr/alerte/CERTFR-2026-ALE-007/){:target="_blank"}
