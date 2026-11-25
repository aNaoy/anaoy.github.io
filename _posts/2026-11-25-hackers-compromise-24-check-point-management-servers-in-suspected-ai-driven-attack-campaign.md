---
title: 'Hackers Compromise 24 Check Point Management Servers in Suspected AI-Driven Attack Campaign'
date: 2026-11-25
permalink: /posts/2026/11/25/hackers-compromise-24-check-point-management-servers-in-suspected-ai-driven-attack-campaign/
tags:
- veille-cyber
- hackernews
---
### Campagne d'attaques automatisées par IA contre les serveurs Check Point

Une campagne de cyberattaques, baptisée **GT13**, a ciblé 24 serveurs de gestion de sécurité Check Point dans 22 organisations mondiales entre octobre et novembre 2026. L'attaquant utilise des outils pilotés par l'IA pour automatiser la reconnaissance, l'exploitation et le mouvement latéral au sein des réseaux victimes.

**Points clés :**
* **Mode opératoire :** Utilisation de 99 adresses IP (VPN et serveurs compromis) et de scripts Python pour automatiser les interactions.
* **Impact :** Vol de bases de données pare-feu et de certificats, neutralisation des politiques de sécurité et usage de serveurs compromis comme relais pour des attaques ultérieures.
* **Secteurs visés :** Finance, énergie, gouvernement, transport, ingénierie et fabrication.

**Vulnérabilités exploitées :**
L'attaquant exploite activement des failles connues pour lesquelles des correctifs sont disponibles :
* **CVE-2026-16232 :** Faille critique dans Check Point permettant l'exécution de tâches de gestion non autorisées.
* **CVE-2026-61500 :** Vulnérabilité dans Rejetto HFS utilisée pour le contrôle initial.
* **Autres cibles récurrentes :** Ivanti Connect Secure (CVE-2024-21893), Citrix NetScaler (CVE-2023-4966, CVE-2025-5777), VMware vCenter (CVE-2021-21972, CVE-2023-34048) et Microsoft Exchange/Netlogon (CVE-2021-26855, CVE-2021-34473, CVE-2020-1472, CVE-2026-41089).

**Recommandations :**
* **Appliquer les correctifs :** Installer immédiatement toutes les mises à jour de sécurité disponibles pour les produits Check Point et les autres logiciels cités.
* **Durcissement :** Suivre les directives de durcissement (hardening) publiées par Check Point pour restreindre l'accès aux serveurs de gestion.
* **Surveillance :** Surveiller les journaux pour détecter toute activité inhabituelle, notamment l'exécution de tâches de gestion non planifiées ou des tentatives d'accès aux fichiers de configuration système.

---
[Source](https://thehackernews.com/2026/11/hackers-compromise-24-check-point.html){:target="_blank"}
