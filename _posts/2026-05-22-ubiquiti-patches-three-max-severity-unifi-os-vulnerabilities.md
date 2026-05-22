---
title: 'Ubiquiti patches three max severity UniFi OS vulnerabilities'
date: 2026-05-22
permalink: /posts/2026/05/22/ubiquiti-patches-three-max-severity-unifi-os-vulnerabilities/
tags:
- veille-cyber
- bleepingcomp
---
### Correction critique de vulnérabilités critiques dans UniFi OS

Ubiquiti a publié des correctifs pour cinq vulnérabilités affectant UniFi OS, dont trois présentant un niveau de gravité maximal. Ces failles permettent à des attaquants distants, sans privilèges, de compromettre les systèmes exposés. Environ 100 000 terminaux UniFi OS sont actuellement accessibles sur Internet, ce qui expose une large surface d'attaque.

**Points clés :**
*   **Accessibilité :** Les vulnérabilités sont exploitables via des attaques de faible complexité ne nécessitant pas d'authentification préalable.
*   **Historique :** Les équipements Ubiquiti sont fréquemment ciblés par des groupes étatiques et des cybercriminels pour la création de botnets (ex: Moobot).
*   **Origine :** Les failles ont été identifiées via le programme de bug bounty HackerOne de l'entreprise.

**Vulnérabilités identifiées :**
*   **CVE-2026-34908 :** Contrôle d'accès inapproprié permettant des modifications non autorisées.
*   **CVE-2026-34909 :** Traversée de répertoire (*Path Traversal*) permettant l'accès à des fichiers système.
*   **CVE-2026-34910 :** Injection de commande via une validation d'entrée insuffisante.
*   **CVE-2026-33000 :** Injection de commande (critique).
*   **CVE-2026-34911 :** Divulgation d'informations (sévérité élevée).

**Recommandations :**
*   **Mise à jour immédiate :** Appliquer sans délai les dernières mises à jour de sécurité fournies par Ubiquiti sur tous les consoles et applications UniFi.
*   **Réduction de la surface d'exposition :** Auditer les équipements UniFi exposés publiquement sur Internet et restreindre l'accès à ces interfaces via un VPN ou un filtrage IP strict si l'accès public n'est pas strictement nécessaire.

---
[Source](https://www.bleepingcomputer.com/news/security/ubiquiti-patches-three-max-severity-unifi-os-vulnerabilities/){:target="_blank"}
