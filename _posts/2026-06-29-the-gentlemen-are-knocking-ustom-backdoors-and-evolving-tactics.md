---
title: 'The Gentlemen are knocking: сustom backdoors and evolving tactics'
date: 2026-06-29
permalink: /posts/2026/06/29/the-gentlemen-are-knocking-ustom-backdoors-and-evolving-tactics/
tags:
- veille-cyber
- securelist
---
### L'essor du groupe "The Gentlemen" : Tactiques et outils malveillants

Le groupe "The Gentlemen", opérant via un modèle Ransomware-as-a-Service (RaaS), est devenu l'un des acteurs les plus actifs depuis 2026, ciblant des infrastructures critiques et de grandes entreprises à travers le monde.

**Points clés :**
*   **Vecteurs d'infection :** Exploitation de vulnérabilités dans les services exposés (VPN, pare-feux) et usage d'identifiants faibles ou compromis.
*   **Reconnaissance :** Utilisation d'outils légitimes détournés (*SharpADWS*, *NetScan*, *Advanced IP Scanner*) et du binaire système *netsh* pour capturer le trafic réseau.
*   **Déplacement latéral :** Usage de scripts PowerShell personnalisés, de *PsExec* et de déploiement via GPO pour infecter massivement le réseau.
*   **Neutralisation des solutions de sécurité :** Recours à la technique **BYOVD** (*Bring Your Own Vulnerable Driver*) pour injecter des pilotes vulnérables et désactiver les EDR/Antivirus.
*   **Outillage spécifique :** Utilisation d'une porte dérobée (*backdoor*) personnalisée en Go et de deux variantes de ransomwares (Go et C) en constante évolution.

**Vulnérabilités exploitées (BYOVD) :**
Le groupe exploite une série de pilotes légitimes présentant des vulnérabilités connues (bien qu'aucune CVE spécifique ne soit citée, les pilotes identifiés incluent des versions vulnérables de *Safetica*, *WatchDog*, *Fedeen/Hotta*, *Paragon*, *Topaz* et *Huawei*).

**Recommandations :**
*   **Gestion des vulnérabilités :** Appliquer les correctifs de sécurité sur tous les équipements exposés à Internet (VPN, firewalls).
*   **Durcissement (Hardening) :** Surveiller l'intégrité des pilotes chargés et restreindre l'exécution des outils d'administration système (*netsh*, *PowerShell*) aux utilisateurs légitimes.
*   **Politique d'accès :** Mettre en œuvre une authentification multi-facteurs (MFA) rigoureuse pour limiter l'impact des identifiants compromis.
*   **Surveillance :** Détecter la création de tâches planifiées suspectes et les modifications non autorisées des clés de registre liées à Windows Defender.
*   **Filtrage :** Bloquer les communications vers les adresses C2 identifiées (ex: `81.177.215[.]15`).

---
[Source](https://securelist.com/the-gentlemen-raas/120447/){:target="_blank"}
