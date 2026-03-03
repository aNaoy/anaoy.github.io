---
title: 'Bruteforce Scans for CrushFTP , (Tue, Mar 3rd)'
date: 2026-03-03
permalink: /posts/2026/03/03/bruteforce-scans-for-crushftp-tue-mar-3rd/
tags:
- veille-cyber
- sans-isc
---
**Campagne de Brute-Force sur CrushFTP**

Une vague d'attaques par force brute cible actuellement les instances de CrushFTP. Ces tentatives ne visent pas des vulnérabilités spécifiques, mais plutôt des configurations par défaut ou peu sécurisées.

Les attaquants exploitent des paires identifiant/mot de passe courantes, notamment "crushadmin" pour le nom d'utilisateur et "crushadmin" pour le mot de passe. Ces informations sont envoyées via des requêtes POST, mais les identifiants sont passés en paramètres GET avec un corps de requête vide.

Ces attaques proviennent d'une adresse IP française (5.189.139.225) qui a déjà été observée tentant d'exploiter des vulnérabilités simples depuis février.

**Points clés :**

*   Attaques par force brute sur CrushFTP.
*   Ciblage des configurations par défaut ou laxistes.
*   Utilisation de noms d'utilisateur et mots de passe courants comme "crushadmin/crushadmin".
*   Les requêtes utilisent des paramètres GET pour les identifiants, avec un corps vide.
*   Origine des attaques : une IP française avec un historique d'activités malveillantes.

**Vulnérabilités antérieures mentionnées (non exploitées dans cette campagne) :**

*   CVE-2024-4040 : Injection de template permettant l'évasion du sandbox VFS et l'exécution de code à distance (RCE).
*   CVE-2025-31161 : Contournement d'authentification menant à la divulgation du compte "crushadmin".
*   CVE-2025-54309 : Vulnérabilité zero-day de juillet 2025, exploitée activement.

**Recommandations :**

*   Éviter d'utiliser les identifiants et mots de passe suggérés par défaut pour le compte administrateur.
*   Implémenter des mots de passe forts et uniques pour tous les comptes.
*   Surveiller les journaux d'activité pour détecter les tentatives d'authentification suspectes.
*   S'assurer que toutes les instances de CrushFTP sont mises à jour avec les derniers correctifs de sécurité.

---
[Source](https://isc.sans.edu/diary/rss/32762){:target="_blank"}
