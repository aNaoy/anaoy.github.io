---
title: 'CISA orders feds to patch max-severity Cisco flaw by Sunday'
date: 2026-03-20
permalink: /posts/2026/03/20/cisa-orders-feds-to-patch-max-severity-cisco-flaw-by-sunday/
tags:
- veille-cyber
- bleepingcomp
---
### Urgence : Correction critique pour Cisco Secure Firewall Management Center

La CISA a imposé aux agences fédérales américaines l'application des correctifs pour une faille de sécurité critique affectant Cisco Secure Firewall Management Center (FMC) avant le dimanche 22 mars. Cette vulnérabilité, déjà activement exploitée par le groupe de rançongiciel « Interlock » depuis fin janvier, permet une prise de contrôle totale des systèmes ciblés.

**Points clés :**
*   **Impact :** L'interface de gestion web des appliances Cisco est vulnérable, exposant des équipements critiques (pare-feux, prévention d'intrusion, filtrage).
*   **Exploitation active :** Le gang Interlock utilise cette faille en tant que *zero-day* depuis plusieurs semaines pour cibler des organisations de santé et des institutions publiques.
*   **Directive officielle :** La faille a été ajoutée au catalogue des vulnérabilités exploitées connues (KEV) de la CISA.

**Vulnérabilité :**
*   **CVE-2026-20131 :** Faille critique de désérialisation non sécurisée d'un flux d'octets Java. Elle permet à un attaquant distant non authentifié d'exécuter du code arbitraire avec des privilèges **root** sur le dispositif.

**Recommandations :**
*   **Application immédiate :** Installer sans délai les mises à jour de sécurité fournies par Cisco.
*   **Absence de contournement :** Cisco a confirmé qu'il n'existe aucune solution de contournement (workaround) ; le correctif logiciel est la seule protection.
*   **Vigilance étendue :** Bien que la directive concerne les agences fédérales, toutes les entreprises et administrations utilisant ces solutions doivent appliquer le correctif en priorité absolue en raison de l'exploitation active par des groupes de rançongiciels.

---
[Source](https://www.bleepingcomputer.com/news/security/cisa-orders-feds-to-patch-max-severity-cisco-flaw-by-sunday/){:target="_blank"}
