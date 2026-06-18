---
title: 'DragonForce Hackers Abuse Microsoft Teams Relays to Hide Backdoor.Turn C2 Traffic'
date: 2026-06-18
permalink: /posts/2026/06/18/dragonforce-hackers-abuse-microsoft-teams-relays-to-hide-backdoorturn-c2-traffic/
tags:
- veille-cyber
- hackernews
---
### Détournement des relais Microsoft Teams par le groupe DragonForce

Le groupe de ransomware DragonForce a déployé une nouvelle porte dérobée baptisée **Backdoor.Turn**, capable de dissimuler son trafic de commande et contrôle (C2) en utilisant l'infrastructure de relais TURN (Traversal Using Relays around NAT) de Microsoft Teams. Cette technique, appelée "Ghost Calls", permet aux attaquants de maintenir une présence persistante sur les réseaux victimes en faisant passer leurs communications pour du trafic légitime vers les serveurs Microsoft.

**Points clés :**
* **Infiltration :** Les attaquants obtiennent un accès initial, probablement via des vulnérabilités SQL ou par l'achat d'accès, avant d'utiliser une attaque par chargement latéral de DLL (DLL side-loading).
* **Technique BYOVD :** Les cybercriminels exploitent la technique "Bring Your Own Vulnerable Driver" pour désactiver les logiciels de sécurité en utilisant des pilotes vulnérables légitimes.
* **Persistance :** La porte dérobée est injectée dans le processus `DbgView64.exe` pour garantir un accès à long terme.
* **Capacités :** Le malware permet l'exécution de commandes, la recherche dans Active Directory, l'analyse réseau et le vol d'identifiants.

**Vulnérabilités exploitées (via BYOVD) :**
* **CVE-2023-52271** (pilote `wsftprm.sys`)
* **CVE-2025-61155** (pilote `GameDriverX64.sys`)
* **CVE-2025-1055** (pilote `K7RKScan.sys`)
* Utilisation du pilote malveillant personnalisé `ABYSSWORKER`.

**Recommandations :**
* **Surveillance réseau :** Bien que le trafic passe par des serveurs Microsoft, surveillez les connexions sortantes inhabituelles ou persistantes vers des terminaux Teams, particulièrement celles initiées par des processus non liés aux applications de communication.
* **Sécurité des pilotes :** Appliquez des politiques de contrôle d'intégrité du noyau (comme *Windows Defender Application Control*) pour bloquer le chargement de pilotes signés mais connus pour être vulnérables.
* **Gestion des accès :** Renforcez la sécurité des serveurs SQL et auditez régulièrement les comptes à privilèges pour prévenir les compromissions initiales.
* **Analyse comportementale :** Détectez les tentatives de désactivation des solutions de sécurité (EDR) et les comportements suspects liés au chargement de DLL non signées.

---
[Source](https://thehackernews.com/2026/06/dragonforce-hackers-abuse-microsoft.html){:target="_blank"}
