---
title: 'UAT-10147 Uses AI to Scale Server Attacks, Deploys SPECTRE With EDR Bypass and Linux Rootkit'
date: 2026-08-24
permalink: /posts/2026/08/24/uat-10147-uses-ai-to-scale-server-attacks-deploys-spectre-with-edr-bypass-and-linux-rootkit/
tags:
- veille-cyber
- hackernews
---
### UAT-10147 : Offensive cybernétique automatisée par l'IA

Le groupe UAT-10147, opérant en langue chinoise, cible des serveurs Windows et Linux à l'échelle mondiale dans divers secteurs (éducation, technologie, gaming). Ce groupe se distingue par l'intégration massive d'outils d'IA (PentestGPT, DeepAudit) pour automatiser chaque phase de la chaîne d'attaque : reconnaissance, validation d'exploits, génération de charges utiles et maintien de la persistance.

#### Points clés
*   **Infrastructure sophistiquée :** Utilisation de listes ciblées de 170 000 URL et exfiltration de données dissimulée dans le trafic de services cloud légitimes pour éviter la détection.
*   **Implant SPECTRE :** Un logiciel malveillant multiplateforme capable de contourner les EDR via des techniques BYOVD (*Bring Your Own Vulnerable Driver*) et des injections de code avancées.
*   **Rootkit Linux :** La version Linux de SPECTRE déploie un rootkit kernel pour assurer un contrôle persistant et invisible au niveau du noyau.
*   **Automatisation :** Usage intensif de scripts Python et de frameworks d'IA pour déboguer les web shells, automatiser l'élévation de privilèges et adapter les attaques aux configurations des victimes.

#### Vulnérabilités exploitées
L'acteur exploite de multiples failles connues pour l'accès initial et l'élévation de privilèges :
*   **Windows / IIS :** CVE-2019-16098 (pilote MSI RTCore64.sys), CVE-2021-21551 (pilote Dell DBUtil_2_3.sys).
*   **Linux :** CVE-2022-0995, CVE-2021-3156, CVE-2015-5287, CVE-2015-3246, CVE-2010-3904, CVE-2022-0847.
*   **Web/Services :** CVE-2022-27925 (Zimbra), CVE-2021-23758 (AjaxPro), CVE-2019-18935 (Telerik), CVE-2021-29441/2 (Alibaba Nacos).

#### Recommandations
1.  **Gestion des correctifs :** Appliquer prioritairement les mises à jour pour les vulnérabilités listées ci-dessus sur tous les serveurs exposés.
2.  **Durcissement du noyau :** Surveiller l'installation de modules kernel non signés et limiter l'utilisation de pilotes vulnérables connus via des politiques de contrôle d'intégrité du code (ex: *Windows Defender Application Control*).
3.  **Surveillance réseau :** Détecter les anomalies dans les flux sortants vers les services cloud, qui pourraient masquer une exfiltration de données.
4.  **Audit des accès :** Vérifier régulièrement la présence de tâches planifiées suspectes (ex: "Google Chrome Start") et de web shells (fichiers `.ashx` ou autres dans les répertoires web).
5.  **Protection EDR :** Configurer les solutions EDR pour bloquer spécifiquement les techniques de BYOVD et surveiller les tentatives de modification de la liste de callbacks du kernel.

---
[Source](https://thehackernews.com/2026/08/uat-10147-uses-ai-to-scale-server.html){:target="_blank"}
