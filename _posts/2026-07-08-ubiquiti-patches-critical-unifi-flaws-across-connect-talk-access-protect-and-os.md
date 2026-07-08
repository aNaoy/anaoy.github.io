---
title: 'Ubiquiti Patches Critical UniFi Flaws Across Connect, Talk, Access, Protect, and OS'
date: 2026-07-08
permalink: /posts/2026/07/08/ubiquiti-patches-critical-unifi-flaws-across-connect-talk-access-protect-and-os/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans l'écosystème Ubiquiti UniFi

Ubiquiti a publié des correctifs de sécurité urgents pour corriger plusieurs failles critiques affectant ses applications UniFi (Connect, Talk, Access, Protect et OS). Ces vulnérabilités, majoritairement classées avec des scores CVSS très élevés, permettent à un attaquant distant ayant accès au réseau d'exécuter des commandes arbitraires, d'élever ses privilèges ou de modifier des configurations.

**Points clés :**
* Les vulnérabilités concernent l'exécution de code à distance (RCE), l'injection SQL, le contournement d'accès (SSRF) et l'injection de commandes.
* Bien qu'aucune exploitation active de ces failles spécifiques n'ait été rapportée à ce jour, Ubiquiti souligne la nécessité d'une mise à jour immédiate au regard de la dangerosité des vecteurs d'attaque.
* Historiquement, les équipements Ubiquiti font régulièrement l'objet de campagnes d'exploitation par des acteurs étatiques (ex: botnet MooBot).

**Vulnérabilités identifiées :**
* **CVE-2026-50746 (Score 10.0) :** Injection de commandes dans *UniFi Connect*.
* **CVE-2026-50747 (Score 9.9) :** Injections SQL dans *UniFi Talk*.
* **CVE-2026-50748 (Score 9.9) :** Injection de commandes dans *UniFi Access*.
* **CVE-2026-55115 (Score 9.9) :** SSRF dans *UniFi Protect*.
* **CVE-2026-54402 (Score 9.9) :** Injection de commandes dans *UniFi OS*.
* **CVE-2026-54400 (Score 9.1) :** Élévation de privilèges dans *UniFi Access*.
* **CVE-2026-55116 (Score 9.0) :** Contrôle d'accès non autorisé dans *UniFi OS*.

**Recommandations :**
* Appliquer immédiatement les mises à jour logicielles vers les versions corrigées :
    * **UniFi Connect :** 3.4.20
    * **UniFi Talk :** 5.2.2
    * **UniFi Access :** 4.2.29
    * **UniFi Protect :** 7.1.83
    * **UniFi OS :** 5.1.19
* Restreindre l'accès réseau aux interfaces de gestion des applications UniFi pour limiter la surface d'exposition aux menaces internes et externes.

---
[Source](https://thehackernews.com/2026/07/ubiquiti-patches-critical-unifi-flaws.html){:target="_blank"}
