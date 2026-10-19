---
title: 'Microsoft: October Windows Server updates break Exchange sign-in, mail flow'
date: 2026-10-19
permalink: /posts/2026/10/19/microsoft-october-windows-server-updates-break-exchange-sign-in-mail-flow/
tags:
- veille-cyber
- bleepingcomp
---
### Dysfonctionnements d'Exchange Server suite aux mises à jour Windows d'octobre 2026

Les mises à jour de sécurité Windows d'octobre 2026 causent des instabilités sur certains serveurs Exchange (Windows Server 2019 et versions ultérieures). Ce problème, qui n'est pas lié aux correctifs spécifiques d'Exchange, découle d'une nouvelle limite de mémoire imposée par l'« Endpoint Mapper », insuffisante pour gérer la charge des serveurs Exchange.

**Points clés :**
* **Symptômes :** Impossibilité de se connecter à Outlook on the Web (OWA), messages bloqués dans la boîte d'envoi et erreurs MapiExceptionMdbOffline (ID d'événement 1006).
* **Cause :** La mise à jour Windows a instauré une limite par défaut de 512 appels simultanés pour l'« Endpoint Lookup », ce qui sature la mémoire sous forte charge.
* **Vulnérabilités :** Aucune CVE associée. Il s'agit d'un problème de configuration système induit par une mise à jour.

**Recommandations :**
* Ne pas désinstaller les mises à jour de sécurité, car elles restent essentielles.
* Appliquer le contournement temporaire via la base de registre en exécutant la commande suivante dans une invite de commande avec privilèges élevés, puis redémarrer le serveur :
  `reg add "HKLM\SOFTWARE\Microsoft\Rpc" /v EpmapSavedContextCap /t REG_DWORD /d 65536 /f`
* Surveiller les performances du serveur après le redémarrage et ajuster à nouveau la limite si les problèmes persistent.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-october-windows-server-updates-cause-exchange-issues/){:target="_blank"}
