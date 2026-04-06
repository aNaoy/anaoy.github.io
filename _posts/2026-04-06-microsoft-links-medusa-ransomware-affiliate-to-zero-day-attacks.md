---
title: 'Microsoft links Medusa ransomware affiliate to zero-day attacks'
date: 2026-04-06
permalink: /posts/2026/04/06/microsoft-links-medusa-ransomware-affiliate-to-zero-day-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Menace Storm-1175 : L'escalade vers l'exploitation de zero-days pour le ransomware Medusa

Le groupe cybercriminel Storm-1175, d'origine chinoise, intensifie ses opérations en exploitant rapidement des vulnérabilités critiques pour déployer le ransomware Medusa. Ce groupe se distingue par sa réactivité extrême, utilisant des failles « N-day » et « zero-day » parfois moins de 24 heures après leur découverte, ou même avant la publication des correctifs. Les secteurs de la santé, de l'éducation et de la finance, principalement au Royaume-Uni, aux États-Unis et en Australie, sont les cibles privilégiées.

**Points clés :**
*   **Rapidité d'exécution :** Passage de l'accès initial à l'exfiltration de données et au déploiement du ransomware en quelques jours.
*   **Mode opératoire :** Chaînage d'exploits pour maintenir la persistance, création de comptes administrateurs, déploiement d'outils de gestion à distance et désactivation des solutions de sécurité.
*   **Expansion des cibles :** Plus de 16 vulnérabilités exploitées récemment sur une dizaine de logiciels différents.

**Vulnérabilités critiques mentionnées (CVE) :**
Le groupe a récemment exploité des vulnérabilités majeures, notamment :
*   **GoAnywhere MFT :** CVE-2025-10035
*   **SmarterMail (Auth Bypass) :** CVE-2026-23760
*   **Autres failles ciblées :** Microsoft Exchange (CVE-2023-21529), Papercut (CVE-2023-27351, CVE-2023-27350), Ivanti Connect Secure (CVE-2023-46805, CVE-2024-21887), ConnectWise ScreenConnect (CVE-2024-1709, CVE-2024-1708), JetBrains TeamCity (CVE-2024-27198, CVE-2024-27199), SimpleHelp (CVE-2024-57726, 57727, 57728), CrushFTP (CVE-2025-31161), SmarterMail (CVE-2025-52691) et BeyondTrust (CVE-2026-1731).

**Recommandations :**
*   **Veille proactive :** Prioriser le « patching » des actifs exposés sur le périmètre (Périmètre réseau) dès l'annonce de nouvelles vulnérabilités.
*   **Gestion des accès :** Surveiller étroitement la création de nouveaux comptes utilisateurs et l'installation de logiciels de gestion à distance non autorisés.
*   **Défense en profondeur :** Maintenir les solutions de sécurité activées et surveiller les comportements anormaux post-authentification.
*   **Hygiène logicielle :** Mettre à jour systématiquement les outils de transfert de fichiers (MFT), les serveurs mails et les outils de collaboration, souvent utilisés comme vecteurs d'entrée par ce groupe.

---
[Source](https://www.bleepingcomputer.com/news/security/microsoft-links-medusa-ransomware-affiliate-to-zero-day-attacks/){:target="_blank"}
