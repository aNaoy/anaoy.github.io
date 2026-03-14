---
title: 'Microsoft: Windows 11 users cant access C: drive on some Samsung PCs'
date: 2026-03-14
permalink: /posts/2026/03/14/microsoft-windows-11-users-cant-access-c-drive-on-some-samsung-pcs/
tags:
- veille-cyber
- bleepingcomp
---
### Blocage d'accès au lecteur C: sur certains ordinateurs Samsung sous Windows 11

Une mise à jour de sécurité de février 2026 provoque des erreurs de type « Accès refusé » sur le lecteur C: de certains ordinateurs Samsung (notamment les Galaxy Book 4), empêchant l'exécution d'applications et l'accès aux fichiers système sous Windows 11 (versions 24H2 et 25H2).

**Points clés :**
* **Symptômes :** Impossibilité d'ouvrir Outlook, Office, les navigateurs ou d'effectuer des tâches administratives.
* **Causes suspectées :** Une interaction conflictuelle entre les mises à jour Windows et l'application *Samsung Share*.
* **Localisation :** Problème principalement rapporté au Brésil, au Portugal, en Corée du Sud et en Inde.
* **Vulnérabilités :** Aucune CVE n'est associée, mais le problème entraîne un blocage opérationnel complet et peut compromettre l'intégrité du système si des manipulations incorrectes sont effectuées.

**Recommandations :**
* **Attente :** Microsoft et Samsung enquêtent activement ; il est fortement recommandé d'attendre un correctif officiel.
* **Attention aux solutions de contournement :** Une méthode circulant sur Reddit suggère de modifier les autorisations du disque C: pour le groupe « Tout le monde » (*Everyone*). **Cette manipulation est vivement déconseillée**, car elle supprime les protections critiques du système (TrustedInstaller/SYSTEM) et expose dangereusement l'appareil.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-windows-11-users-cant-access-c-drive-on-some-samsung-pcs/){:target="_blank"}
