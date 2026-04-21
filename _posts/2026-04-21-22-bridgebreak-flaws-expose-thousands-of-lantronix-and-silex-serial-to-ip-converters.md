---
title: '22 BRIDGE:BREAK Flaws Expose Thousands of Lantronix and Silex Serial-to-IP Converters'
date: 2026-04-21
permalink: /posts/2026/04/21/22-bridgebreak-flaws-expose-thousands-of-lantronix-and-silex-serial-to-ip-converters/
tags:
- veille-cyber
- hackernews
---
### BRIDGE:BREAK : Vulnérabilités critiques dans les convertisseurs série-vers-IP

Des chercheurs de Forescout ont identifié 22 vulnérabilités, baptisées **BRIDGE:BREAK**, affectant les convertisseurs série-vers-Ethernet de Lantronix (séries EDS3000PS et EDS5000) et de Silex (modèle SD330-AC). Environ 20 000 de ces appareils sont exposés mondialement, créant des risques majeurs pour les systèmes de contrôle industriel et les infrastructures critiques.

**Points clés :**
*   **Impact :** Risque de prise de contrôle totale des appareils, d'interruption des communications série, de falsification de données (valeurs de capteurs) et de mouvements latéraux dans le réseau.
*   **Vecteur d'attaque :** Les attaquants peuvent compromettre le convertisseur après avoir accédé au réseau cible via un appareil de périmètre (routeur, pare-feu).

**Vulnérabilités majeures (non exhaustives) :**
*   **Exécution de code à distance (RCE) :** CVE-2026-32955, CVE-2026-32956, CVE-2026-32961, CVE-2025-67041, CVE-2025-67034, CVE-2025-67035, CVE-2025-67036, CVE-2025-67037, CVE-2025-67038.
*   **Contournement d'authentification :** CVE-2026-32960, CVE-2025-67039.
*   **Altération (Firmware/Configuration) :** CVE-2026-32958, CVE-2026-32962, CVE-2026-32964.
*   **Déni de service (DoS) :** CVE-2026-32961, CVE-2015-5621, CVE-2024-24487.
*   **Prise de contrôle :** CVE-2026-32965, CVE-2025-70082, FSCT-2025-0021.

**Recommandations :**
*   **Mise à jour :** Appliquer immédiatement les correctifs firmware fournis par [Lantronix](https://ltrxdev.atlassian.net/wiki/spaces/LTRXTS/pages/1349189633/Latest+Firmware+for+the+EDS3000PS+series) et [Silex](https://www.silex.jp/support/security-advisories/en/2026-001).
*   **Sécurisation des accès :** Modifier les identifiants par défaut et renforcer la robustesse des mots de passe.
*   **Isolation réseau :** Segmenter les réseaux pour empêcher l'accès direct aux convertisseurs depuis l'extérieur.
*   **Exposition :** S'assurer qu'aucun appareil n'est directement accessible via Internet.

---
[Source](https://thehackernews.com/2026/04/22-bridgebreak-flaws-expose-20000.html){:target="_blank"}
