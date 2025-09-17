---
title: 'GOLD SALEM’s Warlock operation joins busy ransomware landscape'
date: 2025-09-17
permalink: /posts/2025/09/17/gold-salems-warlock-operation-joins-busy-ransomware-landscape/
tags:
- veille-cyber
- sophos
---
### L'opération Warlock : une nouvelle menace de ransomware

Le groupe de cybercriminels GOLD SALEM, également connu sous le nom de Warlock Group, s'est imposé sur la scène des ransomwares depuis mars 2025. Bien que Microsoft suggère une origine chinoise pour ce groupe (Storm-2603), les preuves actuelles sont insuffisantes pour le confirmer. GOLD SALEM cible un large éventail d'organisations à travers l'Amérique du Nord, l'Europe et l'Amérique du Sud, et publie les noms de ses victimes ainsi que des données volées sur un site dédié sur le réseau Tor. L'activité du groupe a été remarquée pour la première fois en juin 2025, lorsqu'ils ont activement recherché des exploits pour des applications d'entreprise courantes et des outils capables de désactiver les solutions de sécurité.

#### Points Clés :

*   **Opération Warlock :** Nouvelle menace de ransomware active depuis mars 2025.
*   **Victimologie :** Cible des entités commerciales et gouvernementales de toutes tailles, principalement en dehors de la Chine et de la Russie.
*   **Modus Operandi :** Utilise un site de fuite (DLS) sur Tor pour publier des données volées et réclamer des rançons.
*   **Développement Rapide :** Le groupe a démontré des compétences techniques avancées et une capacité d'adaptation.
*   **Coopération :** Recherche des exploitants de vulnérabilités et des courtiers en accès initial.

#### Vulnérabilités :

*   **Exploitation de SharePoint :** Utilisation de la chaîne d'exploitation ToolShell, exploitant une combinaison de vulnérabilités :
    *   CVE-2025-49704
    *   CVE-2025-49706
    *   CVE-2025-53770
    *   CVE-2025-53771
*   **Contournement de l'EDR :** Utilisation de la technique "Bring Your Own Vulnerable Driver" (BYOVD) avec un pilote Baidu Antivirus vulnérable (CVE-2024-51324) renommé googleApiUtil64.sys pour terminer les agents de détection et de réponse.
*   **Exfiltration de identifiants :** Utilisation de Mimikatz pour cibler la mémoire LSASS afin d'extraire des identifiants en clair.
*   **Mouvements latéraux :** Recours à PsExec et Impacket.
*   **Déploiement de la charge utile :** Utilisation de Group Policy Objects (GPO).
*   **Accès à distance :** Abus de l'outil Velociraptor pour créer un tunnel réseau via Visual Studio Code.

#### Recommandations :

*   **Surveillance de la surface d'attaque :** Mettre en œuvre une surveillance continue des actifs exposés à Internet.
*   **Politiques de patching agressives :** Appliquer rapidement les correctifs aux services exposés à Internet, en particulier pour les vulnérabilités connues comme celles affectant SharePoint.
*   **Surveillance proactive des terminaux :** Utiliser des solutions de sécurité capables de détecter les comportements suspects et les tentatives d'exploitation.
*   **Réponse aux incidents rapide :** Mettre en place des procédures de réponse aux incidents efficaces pour réagir rapidement aux compromissions.
*   **Restrictions d'accès :** Examiner et restreindre les accès en se basant sur les indicateurs de compromission fournis (hashes de fichiers, etc.).

---
[Source](https://news.sophos.com/en-us/2025/09/17/gold-salems-warlock-operation-joins-busy-ransomware-landscape/){:target="_blank"}
