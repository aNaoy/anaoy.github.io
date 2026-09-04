---
title: 'Critical Citrix NetScaler auth bypass now leveraged in attacks'
date: 2026-09-04
permalink: /posts/2026/09/04/critical-citrix-netscaler-auth-bypass-now-leveraged-in-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Exploitation active de la faille critique dans Citrix NetScaler

Des attaquants exploitent actuellement une vulnérabilité critique affectant les appliances Citrix NetScaler, suite à la publication en ligne d'un exploit de type preuve de concept (PoC). Des tentatives d'intrusion ont été détectées provenant de diverses localisations géographiques.

**Vulnérabilité**
*   **CVE-2026-19490** : Faille permettant de contourner l'authentification à distance sur les appliances NetScaler configurées comme serveur virtuel AAA ou Gateway (SSL VPN, ICA Proxy, CVPN, RDP Proxy). La vulnérabilité dépend de la version du firmware et de la configuration de l'action SAML.

**Points clés**
*   La faille expose un nombre important d'appliances accessibles sur Internet (plus de 22 000 serveurs ADC et 1 700 instances Gateway identifiés par Shadowserver).
*   Des chercheurs en sécurité et des centres nationaux de cybersécurité (notamment en Belgique) confirment que des requêtes malveillantes exploitant la faille ont été enregistrées.
*   Citrix a un historique de vulnérabilités rapidement exploitées après la publication de correctifs (comme ce fut le cas pour les CVE-2026-3055 et CVE-2026-4368).

**Recommandations**
*   Consulter immédiatement le bulletin de sécurité officiel de Citrix (CTX696939).
*   Évaluer l'exposition des infrastructures internes et vérifier si les déploiements sont concernés par cette vulnérabilité.
*   Appliquer les mises à jour de firmware recommandées par l'éditeur sans délai.

---
[Source](https://www.bleepingcomputer.com/news/security/hackers-target-critical-citrix-netscaler-auth-bypass-in-attacks/){:target="_blank"}
