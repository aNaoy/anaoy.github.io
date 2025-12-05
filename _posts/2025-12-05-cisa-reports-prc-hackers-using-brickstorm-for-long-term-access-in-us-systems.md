---
title: 'CISA Reports PRC Hackers Using BRICKSTORM for Long-Term Access in U.S. Systems'
date: 2025-12-05
permalink: /posts/2025/12/05/cisa-reports-prc-hackers-using-brickstorm-for-long-term-access-in-us-systems/
tags:
- veille-cyber
- hackernews
---
## BRICKSTORM : La porte dérobée persistante des cybercriminels chinois

Des acteurs parrainés par la République Populaire de Chine utilisent un logiciel malveillant sophistiqué nommé BRICKSTORM pour obtenir et maintenir un accès à long terme aux systèmes compromis, en particulier dans les environnements VMware vSphere et Windows. Ce cheval de Troie, développé en Golang, offre un accès shell interactif, permettant aux attaquants de manipuler des fichiers, de se déplacer latéralement et d'établir des canaux de communication discrets.

BRICKSTORM a été utilisé dans des attaques visant des secteurs gouvernementaux et technologiques, exploitant des vulnérabilités connues telles que celles affectant Ivanti Connect Secure et VMware vCenter. Les groupes, notamment UNC5221 et Warp Panda, sont impliqués dans ces campagnes, démontrant une grande maîtrise technique et une attention particulière à la discrétion pour assurer un accès furtif et persistant.

Les tactiques incluent l'utilisation de web shells pour un accès initial, l'exploitation de protocoles comme RDP et SMB pour le mouvement latéral, la dissimulation des communications via DNS-over-HTTPS (DoH) et l'utilisation de SOCKS proxy. La capacité de BRICKSTORM à se réinstaller et à fonctionner de manière autonome garantit sa persistance même face aux tentatives de détection. De plus, des implants supplémentaires comme Junction et GuestConduit ont été observés, renforçant les capacités d'exfiltration et de tunneling. Les attaquants ciblent également les environnements cloud, y compris Microsoft Azure, pour accéder à des données sensibles via des services comme OneDrive et SharePoint.

### Points Clés :

*   **Outil principal :** BRICKSTORM, une porte dérobée sophistiquée pour VMware vSphere et Windows.
*   **Acteurs :** Acteurs étatiques de la République Populaire de Chine, associés aux groupes UNC5221 et Warp Panda.
*   **Objectif :** Maintenir un accès persistant et discret aux systèmes compromis.
*   **Capacités :** Accès shell interactif, manipulation de fichiers, communications dissimulées (HTTPS, WebSockets, DoH), proxy SOCKS, capacité d'auto-réinstallation.
*   **Techniques :** Exploitation de vulnérabilités edge, mouvement latéral (RDP, SMB), utilisation de web shells, exfiltration de clés cryptographiques, obtention de jetons de session, enregistrement d'appareils MFA.
*   **Cibles :** Secteurs gouvernementaux, technologiques, services juridiques, fournisseurs SaaS, BPO.
*   **Environnements ciblés :** VMware vSphere, environnements cloud (Azure).
*   **Implants supplémentaires :** Junction et GuestConduit.

### Vulnérabilités exploitées (avec CVE si possible) :

*   CVE-2023-46805 (Ivanti Connect Secure)
*   CVE-2024-21887 (Ivanti Connect Secure)
*   CVE-2024-38812 (VMware vCenter)
*   CVE-2023-34048 (VMware vCenter)
*   CVE-2021-22005 (VMware vCenter)
*   CVE-2023-46747 (F5 BIG-IP)

### Recommandations :

Bien que l'article ne détaille pas explicitement des recommandations pour les victimes, il est implicite que les mesures suivantes sont cruciales :

*   **Mise à jour des systèmes :** Appliquer les correctifs de sécurité pour les logiciels vulnérables, notamment Ivanti Connect Secure et VMware vCenter.
*   **Surveillance du réseau :** Renforcer la détection et la surveillance des activités suspectes, en particulier celles impliquant des communications inhabituelles ou des mouvements latéraux.
*   **Sécurisation des identifiants :** Protéger rigoureusement les identifiants de connexion et les comptes de service.
*   **Gestion des accès :** Examiner et restreindre les privilèges d'accès, en particulier pour les comptes privilégiés et les accès aux environnements virtualisés et cloud.
*   **Analyse des journaux :** Examiner les journaux système et d'application pour détecter les artefacts liés à BRICKSTORM et aux autres implants.
*   **Protection des points d'accès :** Sécuriser les dispositifs réseau exposés à Internet pour empêcher l'accès initial par les attaquants.

---
[Source](https://thehackernews.com/2025/12/cisa-reports-prc-hackers-using.html){:target="_blank"}
