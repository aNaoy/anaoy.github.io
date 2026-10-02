---
title: 'Warlock ransomware breach SharePoint in water, telecom operator attacks'
date: 2026-10-02
permalink: /posts/2026/10/02/warlock-ransomware-breach-sharepoint-in-water-telecom-operator-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Campagne de cyberattaques du groupe Warlock via SharePoint

Le groupe de ransomware Warlock (identifié sous le nom « Longlegs » par Symantec) mène une campagne offensive ciblant les infrastructures critiques (eau, télécoms, universités et gouvernements) dans les pays lusophones et hispanophones. Le groupe utilise des vulnérabilités SharePoint pour s'introduire dans les réseaux, neutraliser les solutions de sécurité et déployer son ransomware à grande échelle.

**Points clés de l'attaque :**
*   **Vecteur initial :** Exploitation de failles SharePoint pour déployer des web shells.
*   **Propagation :** Utilisation du partage SYSVOL pour distribuer le ransomware via des scripts de connexion ou des objets de stratégie de groupe (GPO), permettant une exécution simultanée sur l'ensemble du réseau.
*   **Techniques d'accès distant :** Installation de Visual Studio Code (version Insiders) configuré avec ses capacités de tunnellisation pour maintenir un accès persistant.
*   **Outils tiers :** Utilisation de l'outil *NetExec* pour l'énumération Active Directory et le mouvement latéral.
*   **Neutralisation EDR :** Déploiement d'un outil de désactivation des solutions de protection (AV/EDR) via la technique BYOVD (*Bring Your Own Vulnerable Driver*).

**Vulnérabilités exploitées :**
*   **CVE-2025-49704, CVE-2025-49706, CVE-2025-53770, CVE-2025-53771 :** Chaîne de vulnérabilités « ToolShell » dans Microsoft SharePoint utilisée pour l'exécution de code à distance.
*   **CVE-2025-1055 :** Vulnérabilité présente dans le pilote signé *K7RKScan*, exploitée pour le chargement d'un driver vulnérable (BYOVD) afin de supprimer les protections EDR.

**Recommandations :**
*   **Mise à jour immédiate :** Appliquer tous les correctifs disponibles pour les déploiements SharePoint sur site.
*   **Surveillance du BYOVD :** Bloquer le chargement de pilotes connus comme vulnérables via les politiques de contrôle de l'intégrité du code (Windows Defender Application Control).
*   **Audit SYSVOL :** Surveiller les modifications suspectes dans les partages SYSVOL, souvent utilisés pour stocker des charges utiles (payloads) malveillantes.
*   **Gestion des accès :** Restreindre l'installation et l'exécution d'outils de développement (comme VS Code) sur les serveurs critiques et surveiller les connexions sortantes via des services de tunnellisation.

---
[Source](https://www.bleepingcomputer.com/news/security/warlock-ransomware-breach-sharepoint-in-water-telecom-operator-attacks/){:target="_blank"}
