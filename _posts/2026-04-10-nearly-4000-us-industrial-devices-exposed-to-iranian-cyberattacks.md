---
title: 'Nearly 4,000 US industrial devices exposed to Iranian cyberattacks'
date: 2026-04-10
permalink: /posts/2026/04/10/nearly-4000-us-industrial-devices-exposed-to-iranian-cyberattacks/
tags:
- veille-cyber
- bleepingcomp
---
### Menace iranienne sur les infrastructures critiques américaines

Des groupes de pirates informatiques liés à l'Iran ciblent activement les contrôleurs logiques programmables (PLC) de Rockwell Automation/Allen-Bradley au sein des infrastructures critiques américaines depuis mars 2026. Ces attaques entraînent des perturbations opérationnelles et le vol de données sensibles.

**Points clés :**
*   **Surface d'exposition :** Environ 5 200 appareils PLC sont exposés sur Internet à l'échelle mondiale, dont près de 3 900 (75 %) se situent aux États-Unis.
*   **Vecteurs d'attaque :** Les attaquants exploitent des dispositifs connectés, souvent via des modems cellulaires, pour extraire des fichiers de projet et manipuler les interfaces SCADA/HMI.
*   **Contexte :** Cette campagne s'inscrit dans une escalade des tensions géopolitiques impliquant l'Iran, les États-Unis et Israël. Elle rappelle les modes opératoires passés du groupe CyberAv3ngers (2023-2024).

**Vulnérabilités :**
*   L'article ne mentionne pas de CVE spécifique, mais pointe une vulnérabilité structurelle majeure : l'exposition directe de systèmes de contrôle industriel (OT) sur Internet via le protocole EtherNet/IP (EIP).

**Recommandations :**
*   **Isolation réseau :** Déconnecter les PLC d'Internet ou les protéger systématiquement derrière un pare-feu.
*   **Sécurisation des accès :** Imposer l'authentification multifacteur (MFA) pour tout accès aux réseaux OT.
*   **Surveillance :** Analyser les journaux pour détecter toute activité malveillante et surveiller le trafic suspect sur les ports OT, particulièrement en provenance de l'étranger.
*   **Maintenance :** Mettre à jour les firmwares des appareils, désactiver les services inutilisés et restreindre les méthodes d'authentification obsolètes.

---
[Source](https://www.bleepingcomputer.com/news/security/nearly-4-000-us-industrial-devices-exposed-to-iranian-cyberattacks/){:target="_blank"}
