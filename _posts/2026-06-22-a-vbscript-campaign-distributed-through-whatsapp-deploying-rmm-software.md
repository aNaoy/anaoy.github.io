---
title: 'A VBScript campaign distributed through WhatsApp deploying RMM software'
date: 2026-06-22
permalink: /posts/2026/06/22/a-vbscript-campaign-distributed-through-whatsapp-deploying-rmm-software/
tags:
- veille-cyber
- securelist
---
### Campagne de malwares via WhatsApp : détournement d'outils RMM

Une campagne de cyberattaques active depuis juin 2026 utilise des comptes WhatsApp compromis pour propager des fichiers VBScript malveillants. Masqués sous des noms de documents financiers ou administratifs trompeurs (factures, notes de dette), ces scripts infectent les utilisateurs de WhatsApp Desktop et Web pour déployer un logiciel de gestion à distance (RMM) légitime, *ManageEngine Endpoint Central*, utilisé ici à des fins malveillantes.

**Points clés :**
*   **Mode opératoire :** L'attaquant utilise des comptes compromis pour envoyer des fichiers `.vbs` à la liste de contacts des victimes. L'infection nécessite deux interactions de l'utilisateur (téléchargement puis exécution du fichier).
*   **Chaîne d'infection :** Le VBScript initial télécharge des charges utiles secondaires, modifie les paramètres de contrôle de compte d'utilisateur (UAC) pour s'octroyer des privilèges administratifs, puis installe silencieusement l'agent RMM.
*   **Ciblage :** Campagne opportuniste mondiale (notamment en Malaisie, Brésil, Inde, Mexique, Espagne, etc.) visant des particuliers.
*   **Attribution :** Des indices techniques (commentaires en chinois simplifié, infrastructure partagée avec *ValleyRAT* et *Gh0st RAT*) suggèrent, avec une faible confiance, l'implication d'un acteur utilisant des outils ou des serveurs liés à des groupes chinois.

**Vulnérabilités :**
*   L'attaque n'exploite pas de CVE spécifique, mais abuse des fonctionnalités légitimes de Windows (WScript.exe, `runas`, `bitsadmin`, `curl`) et du détournement de logiciels de gestion à distance (RMM) pour maintenir une persistance.

**Recommandations :**
*   **Sensibilisation :** Ne jamais ouvrir de fichiers exécutables ou de scripts reçus via messagerie, même s'ils semblent provenir d'un contact de confiance.
*   **Filtrage :** Bloquer ou sensibiliser les utilisateurs sur les extensions de fichiers à haut risque : `.vbs`, `.vbe`, `.exe`, `.bat`, `.cmd`, `.js`, `.ps1`.
*   **Sécurité des terminaux :** Appliquer le principe du moindre privilège en limitant les droits d'administration sur les postes de travail.
*   **Surveillance :** Surveiller l'exécution de processus suspects via `WScript.exe` et vérifier les installations inattendues de logiciels de type RMM (comme *ManageEngine Endpoint Central*) dans les environnements où ils ne sont pas explicitement gérés par l'équipe informatique.

---
[Source](https://securelist.com/whatsapp-vbs-rmm-campaign/120290/){:target="_blank"}
