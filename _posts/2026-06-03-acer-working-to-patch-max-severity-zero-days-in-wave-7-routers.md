---
title: 'Acer working to patch max severity zero-days in Wave 7 routers'
date: 2026-06-03
permalink: /posts/2026/06/03/acer-working-to-patch-max-severity-zero-days-in-wave-7-routers/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilités critiques sur les routeurs Acer Wave 7

Acer a identifié deux failles de sécurité « zero-day » de sévérité maximale affectant ses routeurs Wi-Fi Mesh Wave 7 (firmware version T7c_GBL_1.01.000055 et antérieures). Ces vulnérabilités permettent à des attaquants non authentifiés de prendre le contrôle total des équipements.

**Points clés :**
*   **Vulnérabilités :**
    *   **CVE-2026-49200 (Accès non authentifié) :** Un défaut de contrôle d'accès permet de récupérer des identifiants en clair (Web/Telnet) stockés dans les journaux système via l'interface web.
    *   **CVE-2026-49201 (Backdoor persistante) :** La présence d'une clé de chiffrement AES codée en dur dans le binaire `upload.cgi` permet de manipuler les sauvegardes système pour injecter des portes dérobées.
*   **Disponibilité des correctifs :** Aucune mise à jour n'est disponible pour le moment. Acer prévoit une résolution par firmware d'ici la fin du mois de juin 2026.

**Recommandations :**
*   **Atténuation immédiate :** Désactivez la gestion à distance (Remote Management) sur vos routeurs ou, à défaut, restreignez l'accès distant aux seules adresses IP de confiance.
*   **Maintenance :** Surveillez la publication du correctif et mettez à jour le firmware dès sa disponibilité via l'interface d'administration (*System Management* > *Firmware Update*).

---
[Source](https://www.bleepingcomputer.com/news/security/acer-warns-of-max-severity-zero-days-affecting-wave-7-routers/){:target="_blank"}
