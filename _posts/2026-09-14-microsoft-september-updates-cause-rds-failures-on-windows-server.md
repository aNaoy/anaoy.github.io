---
title: 'Microsoft: September updates cause RDS failures on Windows Server'
date: 2026-09-14
permalink: /posts/2026/09/14/microsoft-september-updates-cause-rds-failures-on-windows-server/
tags:
- veille-cyber
- bleepingcomp
---
### Dysfonctionnements des services Bureau à distance (RDS) suite aux mises à jour de septembre 2026

Les mises à jour de sécurité publiées par Microsoft en septembre 2026 provoquent des instabilités majeures dans les services Bureau à distance (RDS) sur une large gamme de systèmes Windows.

**Points clés :**
* **Impact :** Les serveurs (Windows Server 2012 et versions ultérieures) ainsi que les postes clients (Windows 10 et 11) sont touchés.
* **Symptômes :** Échecs de connexion RDP, blocage du processus de session (« Please wait for the Remote Desktop Configuration »), et instabilité d'outils annexes comme l'Explorateur de fichiers ou la console de gestion MMC.
* **Vulnérabilités :** Aucune CVE spécifique n'est associée à cet incident, il s'agit d'une régression logicielle causée par les correctifs de sécurité « Patch Tuesday ».
* **Persistance :** Une fois le problème survenu, les sessions existantes peuvent se bloquer, nécessitant parfois un redémarrage forcé de la machine.

**Recommandations :**
* **Déploiement des correctifs (KIR) :** Microsoft a mis à disposition des fichiers « Known Issue Rollback » (KIR) via des stratégies de groupe (GPO) pour annuler spécifiquement la modification causant le dysfonctionnement sans supprimer l'intégralité des mises à jour de sécurité.
* **Solution de contournement temporaire :** Le redémarrage de la machine virtuelle peut rétablir momentanément l'accès RDP.
* **Alternative déconseillée :** Bien que la désinstallation complète des mises à jour restaure le service, cette méthode est déconseillée car elle expose les systèmes aux vulnérabilités que les correctifs de septembre étaient censés combler.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-september-updates-cause-rds-failures-on-windows-server/){:target="_blank"}
