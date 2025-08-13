---
title: 'Zoom and Xerox Release Critical Security Updates Fixing Privilege Escalation and RCE Flaws'
date: 2025-08-13
permalink: /posts/2025/08/13/zoom-and-xerox-release-critical-security-updates-fixing-privilege-escalation-and-rce-flaws/
tags:
- veille-cyber
- hackernews
---
**Mises à jour de sécurité critiques pour Zoom et Xerox**

Zoom et Xerox ont corrigé des failles de sécurité majeures dans leurs produits Zoom Clients pour Windows et FreeFlow Core.

**Points Clés :**

*   **Zoom Clients pour Windows :** Une vulnérabilité (CVE-2025-49457, score CVSS 9.6) permettait une escalade de privilèges via un chemin de recherche non fiable. Elle pouvait être exploitée par un utilisateur non authentifié via le réseau.
*   **Xerox FreeFlow Core :** Plusieurs vulnérabilités ont été corrigées, dont une (CVE-2025-8356, score CVSS 9.8) de traversée de chemin menant à l'exécution de code à distance (RCE) et une autre (CVE-2025-8355, score CVSS 7.5) de type XML External Entity (XXE) menant à une falsification de requête côté serveur (SSRF).

**Vulnérabilités Spécifiques :**

*   **Zoom :**
    *   CVE-2025-49457 : Escalade de privilèges via un chemin de recherche non fiable.
*   **Xerox :**
    *   CVE-2025-8355 : Injection XXE entraînant du SSRF.
    *   CVE-2025-8356 : Traversée de chemin menant à l'exécution de code à distance.

**Produits Affectés :**

*   **Zoom :** Zoom Workplace pour Windows (versions antérieures à 6.3.10), Zoom Workplace VDI pour Windows (versions antérieures à 6.3.10, sauf 6.1.16 et 6.2.12), Zoom Rooms pour Windows (versions antérieures à 6.3.10), Zoom Rooms Controller pour Windows (versions antérieures à 6.3.10), Zoom Meeting SDK pour Windows (versions antérieures à 6.3.10).
*   **Xerox :** FreeFlow Core (versions antérieures à 8.0.4).

**Recommandations :**

*   **Zoom :** Installer la version 6.3.10 ou ultérieure des clients Zoom pour Windows affectés.
*   **Xerox :** Installer la version 8.0.4 ou ultérieure de Xerox FreeFlow Core.

Ces vulnérabilités, jugées faciles à exploiter, pourraient permettre à un attaquant d'exécuter des commandes arbitraires, de voler des données sensibles ou de se déplacer latéralement dans un environnement d'entreprise.

---
[Source](https://thehackernews.com/2025/08/zoom-and-xerox-release-critical.html){:target="_blank"}
