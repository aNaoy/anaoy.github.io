---
title: 'New Lotus data wiper used against Venezuelan energy, utility firms'
date: 2026-04-21
permalink: /posts/2026/04/21/new-lotus-data-wiper-used-against-venezuelan-energy-utility-firms/
tags:
- veille-cyber
- bleepingcomp
---
### Lotus : Un nouveau malware destructeur ciblant l'énergie au Venezuela

Un nouveau malware de type « wiper » (effaceur de données), baptisé Lotus, a été identifié lors d'attaques ciblées contre des infrastructures énergétiques et de services publics au Venezuela fin 2025. Ce logiciel malveillant est conçu pour rendre les systèmes totalement irrécupérables en écrasant physiquement les disques et en supprimant toute trace d'activité.

**Points clés :**
* **Mode opératoire :** L'attaque commence par des scripts batch (`OhSyncNow.bat`, `notesreg.bat`) qui affaiblissent la sécurité, désactivent les interfaces réseau et les sessions actives.
* **Destruction totale :** Le malware utilise des outils légitimes (Windows `diskpart`, `robocopy`, `fsutil`) pour saturer les disques et écraser les données avant de déployer le payload Lotus.
* **Techniques avancées :** Lotus interagit avec les disques via des appels IOCTL pour effacer les points de restauration, vider le journal USN et écraser physiquement tous les secteurs des disques avec des zéros.
* **Contexte :** L'activité coïncide avec des tensions géopolitiques régionales majeures, notamment une cyberattaque contre la compagnie pétrolière PDVSA.

**Vulnérabilités exploitées :**
* Aucune CVE spécifique n'est mentionnée ; le malware exploite le détournement de privilèges administratifs et l'usage détourné d'outils d'administration système natifs de Windows.

**Recommandations :**
* **Surveillance active :** Détecter toute manipulation anormale du service `UI0Detect`, des modifications suspectes sur le partage `NETLOGON` ou des changements de masse sur les comptes utilisateurs.
* **Analyse comportementale :** Surveiller l'utilisation inhabituelle des commandes `diskpart`, `robocopy` et `fsutil` par des processus non autorisés.
* **Sauvegardes :** Maintenir des sauvegardes régulières conservées hors ligne (air-gapped) et tester systématiquement leur capacité de restauration pour contrer les effets des wipers.

---
[Source](https://www.bleepingcomputer.com/news/security/new-lotus-data-wiper-used-against-venezuelan-energy-utility-firms/){:target="_blank"}
