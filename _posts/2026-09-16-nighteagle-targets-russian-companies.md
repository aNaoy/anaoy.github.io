---
title: 'NightEagle targets Russian companies'
date: 2026-09-16
permalink: /posts/2026/09/16/nighteagle-targets-russian-companies/
tags:
- veille-cyber
- securelist
---
### Expansion des opérations du groupe APT NightEagle vers la Russie

Le groupe APT NightEagle (APT-Q-95) a étendu ses activités depuis l'Asie vers des entreprises en Russie. Ce groupe utilise des tactiques sophistiquées reposant sur des outils légitimes détournés et l'exploitation de vulnérabilités connues pour maintenir sa persistance et se déplacer latéralement au sein des réseaux.

**Points clés :**
*   **Accès initial :** Utilisation d'identifiants valides compromis pour accéder aux VPN d'entreprise, souvent via des tunnels Cloudflare WARP.
*   **Backdoor GhostContainer :** Déploiement d'un backdoor sur les serveurs Microsoft Exchange, utilisant des composants open-source (Neo-reGeorg) et des techniques d'injection dans le paramètre `VIEWSTATE`.
*   **Tunnelisation et mouvements latéraux :** Utilisation de Microsoft Dev Tunnels et de l'outil `rdp2tcp` pour créer des accès distants (RDP) persistants, dissimulés sous des noms de fichiers légitimes (ex: `adobe_32.exe`, `1cbroker.exe`).
*   **Attaque Active Directory :** Exploitation de vulnérabilités pour élever les privilèges et exécution d'attaques de type DCSync pour compromettre les contrôleurs de domaine.

**Vulnérabilités exploitées :**
*   **CVE-2020-0688 :** Exploitation utilisée dans le cadre de la backdoor GhostContainer sur Microsoft Exchange.
*   **CVE-2019-0708 (BlueKeep) :** Exploitation via le protocole RDP pour créer des comptes locaux et obtenir des accès privilégiés.

**Recommandations :**
*   **Surveillance renforcée :** Détecter les anomalies dans les journaux Windows, notamment les événements RDP (IDs 132 et 148) indiquant l'utilisation de canaux suspects par `rdp2tcp`.
*   **Gestion des accès :** Appliquer le principe du moindre privilège, sécuriser les accès VPN par une authentification multi-facteurs (MFA) robuste et réinitialiser les identifiants compromis.
*   **Patch Management :** S'assurer que les correctifs pour les vulnérabilités critiques (en particulier CVE-2020-0688 et CVE-2019-0708) sont appliqués sur tous les serveurs exposés.
*   **Détection :** Mettre en place des règles de détection EDR pour surveiller l'exécution de processus suspects, le chargement de DLL via PowerShell et les tentatives de réplication de données AD (DCSync).

---
[Source](https://securelist.com/tr/nighteagle-apt-ghostcontainer-and-tunneling/121323/){:target="_blank"}
