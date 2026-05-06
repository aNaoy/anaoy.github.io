---
title: 'MuddyWater hackers use Chaos ransomware as a decoy in attacks'
date: 2026-05-06
permalink: /posts/2026/05/06/muddywater-hackers-use-chaos-ransomware-as-a-decoy-in-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Espionnage sous couvert de ransomware : L'opération MuddyWater

Le groupe de cyber-espionnage iranien MuddyWater (alias Static Kitten, Mango Sandstorm) utilise le ransomware « Chaos » comme leurre pour masquer des activités d'espionnage industriel et politique. Cette stratégie vise à brouiller les pistes en faisant passer une intrusion étatique pour une attaque cybercriminelle à but lucratif.

**Points clés :**
* **Détournement de marque :** L'utilisation du ransomware Chaos est une façade ; les techniques déployées indiquent une recherche de persistance et d'exfiltration de données plutôt qu'un gain financier.
* **Vecteur initial :** Ingénierie sociale via Microsoft Teams, incluant des sessions de partage d'écran pour voler des identifiants et contourner la double authentification (MFA).
* **Outils d'accès :** Utilisation massive d'outils d'accès distant légitimes (AnyDesk, DWAgent, RDP) pour maintenir la persistance.
* **Malware personnalisé :** Déploiement d'une porte dérobée (*backdoor*) nommée `Game.exe`, dissimulée sous l'apparence d'une application Microsoft WebView2, dotée de capacités anti-analyse et anti-VM.

**Vulnérabilités :**
* L'attaque repose principalement sur l'exploitation de facteurs humains et de processus de support (ingénierie sociale via Microsoft Quick Assist, manipulation de sessions Teams). Aucune CVE spécifique n'est mentionnée, car l'attaque privilégie l'abus de fonctionnalités légitimes (*Living off the Land*).

**Recommandations :**
* **Sécurisation des communications :** Renforcer la vigilance sur les demandes de partage d'écran ou d'assistance à distance non sollicitées, particulièrement via Microsoft Teams.
* **Audit des accès distants :** Restreindre et surveiller l'utilisation d'outils d'accès distant (AnyDesk, DWAgent, Quick Assist).
* **Protection des identifiants :** Imposer l'utilisation de clés de sécurité matérielles (FIDO2) pour rendre le contournement de l'authentification multifacteur (MFA) beaucoup plus difficile pour les attaquants.
* **Surveillance EDR :** Détecter les exécutions suspectes de fichiers comme `ms_upd.exe` ou `Game.exe`, et surveiller les tentatives de modification des paramètres de sécurité locaux par des comptes utilisateurs.

---
[Source](https://www.bleepingcomputer.com/news/security/muddywater-hackers-use-chaos-ransomware-as-a-decoy-in-attacks/){:target="_blank"}
