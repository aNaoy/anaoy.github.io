---
title: 'DFIR Report – The Gentlemen & SystemBC: A Sneak Peek Behind the Proxy'
date: 2026-04-20
permalink: /posts/2026/04/20/dfir-report-the-gentlemen-systembc-a-sneak-peek-behind-the-proxy/
tags:
- veille-cyber
- zerodaysfans
---
### Analyse de la menace : Le RaaS "The Gentlemen" et SystemBC

Le groupe de ransomware-as-a-service (RaaS) « The Gentlemen », apparu mi-2025, affiche une montée en puissance rapide avec plus de 320 victimes déclarées. Ce collectif cible les environnements d'entreprise (Windows, Linux, NAS, BSD et ESXi) en utilisant des outils de chiffrement développés en Go et C.

**Points clés :**
* **Infrastructures multi-plateformes :** Le RaaS propose des lockers adaptés à divers environnements, incluant des mécanismes de chiffrement partiel pour accélérer l'impact (1% à 9% des fichiers).
* **Déploiement massif :** Utilisation intensive des objets de stratégie de groupe (GPO) pour une exécution simultanée à l'échelle du domaine.
* **Association avec SystemBC :** Des affiliés utilisent le proxy malware *SystemBC* pour établir des tunnels SOCKS5, faciliter le pivotement interne et le téléchargement de charges utiles supplémentaires. Un botnet de plus de 1 570 victimes a été identifié.
* **Extorsion double :** Le groupe menace de publier les données volées via un site dédié (.onion) et utilise des comptes sur les réseaux sociaux pour accentuer la pression.

**Vulnérabilités et vecteurs d'attaque :**
Bien que le vecteur d'accès initial ne soit pas précisé, l'analyse révèle une exploitation poussée des faiblesses suivantes :
* **Déploiement via GPO :** Abus des capacités d'administration légitimes pour distribuer le ransomware.
* **Mise en péril des défenses :** Utilisation de PowerShell pour désactiver Windows Defender (`Set-MpPreference -DisableRealtimeMonitoring $true`) et le pare-feu Windows, ainsi que pour modifier les paramètres LSA (accès anonyme).
* **Outils d'accès distant :** Installation persistante d'AnyDesk et de Cobalt Strike pour maintenir l'accès.

**Recommandations de sécurité :**
* **Restreindre les GPO :** Auditer les autorisations de modification des GPO et limiter l'accès aux comptes ayant des droits d'administration de domaine.
* **Surveillance EDR :** Détecter les exécutions suspectes de `powershell.exe` tentant de modifier les préférences Defender ou d'ajouter des exclusions (`Add-MpPreference`).
* **Durcissement réseau :** Surveiller le trafic vers des serveurs C&C connus (ex: `45.86.230[.]112`, `91.107.247[.]163`) et détecter les tunnels SOCKS5 anormaux.
* **Protection ESXi :** Maintenir les hyperviseurs à jour, restreindre l'accès à SSH/`esxcli` et surveiller la création de tâches `cron` ou de scripts dans `/etc/rc.local.d/`.
* **Gestion des privilèges :** Appliquer le principe du moindre privilège pour limiter l'utilisation de Mimikatz et le dump de credentials en mémoire.

---
[Source](https://research.checkpoint.com/2026/dfir-report-the-gentlemen/){:target="_blank"}
