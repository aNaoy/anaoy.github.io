---
title: 'FBI Warns Russian Intelligence Hackers Target Signal Backup Recovery Keys'
date: 2026-06-27
permalink: /posts/2026/06/27/fbi-warns-russian-intelligence-hackers-target-signal-backup-recovery-keys/
tags:
- veille-cyber
- hackernews
---
### Alerte : Campagne de phishing russe ciblant les clés de récupération Signal

Des services de renseignement russes (groupes identifiés sous les noms **UNC5792** et **UNC4221**) mènent une campagne sophistiquée d'ingénierie sociale visant des cibles à haute valeur ajoutée (officiels, journalistes, militaires). Contrairement aux attaques précédentes, les assaillants ne cherchent plus seulement des codes SMS, mais incitent désormais les utilisateurs à divulguer leur **clé de récupération de sauvegarde Signal** (Signal Backup Recovery Key).

**Points clés :**
* **Méthode :** Les attaquants se font passer pour le support technique de Signal via des messages in-app. Ils utilisent des scénarios de « mise à jour de sécurité » ou de « récupération de données » pour convaincre la victime de leur transmettre sa clé de récupération.
* **Impact :** Une fois en possession de cette clé, les pirates peuvent restaurer la sauvegarde de la victime, accéder à l'historique complet des messages privés et de groupe, et prendre le contrôle du compte, même si celui-ci est réactivé sur un nouveau numéro.
* **Portée :** L'application Signal reste sécurisée techniquement ; l'attaque repose uniquement sur l'ingénierie sociale pour contourner les protections logiques.
* **Vulnérabilité :** Il n'existe pas de CVE spécifique, car il s'agit d'un détournement d'une fonctionnalité légitime de l'application via une manipulation humaine (absence de faille logicielle).

**Recommandations :**
* **Méfiance absolue :** Signal ne contacte jamais ses utilisateurs via la messagerie in-app pour demander des codes, des PIN ou des clés de récupération.
* **Protection des données :** Ne jamais copier ou partager sa clé de récupération de sauvegarde dans une discussion.
* **Audit de sécurité :** Vérifier régulièrement la liste des « Appareils associés » (Linked Devices) dans les paramètres et supprimer toute connexion suspecte.
* **Action en cas de compromission :** Si la clé a été divulguée, il est impératif de générer immédiatement une nouvelle clé de récupération dans les paramètres. Cela invalidera la clé compromise pour les sauvegardes futures (tout en admettant que les données antérieures sont potentiellement exposées).

---
[Source](https://thehackernews.com/2026/06/fbi-warns-russian-intelligence-hackers.html){:target="_blank"}
