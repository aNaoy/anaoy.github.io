---
title: 'Infection repeatedly adds scheduled tasks and increases traffic to the same C2 domain, (Wed, Jan 14th)'
date: 2026-01-14
permalink: /posts/2026/01/14/infection-repeatedly-adds-scheduled-tasks-and-increases-traffic-to-the-same-c2-domain-wed-jan-14th/
tags:
- veille-cyber
- sans-isc
---
## Récurrence et Augmentation du Trafic C2 Post-Infection par Lumma Stealer

Les infections récentes par Lumma Stealer présentent un schéma d'activité post-exfiltration des données. Après avoir volé des informations, le logiciel malveillant récupère une commande PowerShell à partir d'un lien Pastebin, initiant ainsi une nouvelle infection. Celle-ci utilise des domaines en `.cc` pour la communication avec le serveur de commande et de contrôle (C2).

L'exemple observé le 14 janvier 2026 illustre ce comportement. Le lien Pastebin conduit à l'exécution d'une commande PowerShell via `irm` (Invoke-RestMethod). Cette commande, après téléchargement d'un fichier (ici nommé `Notes.pdf`), utilise `mshta` pour exécuter du code à partir du domaine de C2, `fileless-market[.]cc`.

Ce processus se répète de manière cumulative : `mshta` est utilisé pour générer des tâches planifiées qui exécutent à nouveau la même commande `mshta` pointant vers le même domaine C2. En l'espace de 11 heures, 31 tâches planifiées avec des noms différents mais le même déclencheur et la même action ont été observées sur un hôte infecté. Cette multiplication de tâches a entraîné une augmentation significative du trafic HTTPS vers `fileless-market[.]cc`, avec 33 flux TCP identifiés vers ce serveur dans l'exemple étudié. Cette forme d'auto-amplification de l'activité C2 semble inhabituelle.

**Points clés :**

*   **Modèle d'infection récurrent :** Lumma Stealer déclenche une seconde phase d'infection via Pastebin.
*   **Communication C2 persistante :** Utilisation de domaines en `.cc` pour la communication.
*   **Auto-amplification :** Création répétée de tâches planifiées pour augmenter le trafic vers le serveur C2.
*   **Outils utilisés :** `irm`, `mshta`, PowerShell, Tâches planifiées.

**Vulnérabilités :**

Aucune vulnérabilité CVE spécifique n'est mentionnée dans cet article. L'infection exploite des mécanismes de téléchargement et d'exécution de code (via des URL et des scripts) et des fonctionnalités légitimes de Windows (tâches planifiées).

**Recommandations :**

Bien que l'article ne fournisse pas de recommandations directes, les comportements observés suggèrent les mesures suivantes :

*   **Surveillance du trafic réseau :** Porter une attention particulière aux requêtes sortantes vers des domaines suspects, notamment ceux hébergés sur des TLDs comme `.cc`.
*   **Analyse des tâches planifiées :** Vérifier régulièrement les tâches planifiées sur les systèmes Windows pour détecter des entrées inhabituelles ou récurrentes.
*   **Blocage des domaines et URL malveillants :** Mettre à jour les listes de blocage pour inclure les domaines de C2 identifiés (`fileless-market[.]cc`).
*   **Contrôle des accès aux sites externes :** Restreindre ou surveiller les téléchargements et exécutions de scripts provenant de sources externes non fiables, y compris les plateformes comme Pastebin.
*   **Analyse et détection avancée :** Utiliser des solutions de sécurité capables de détecter des schémas d'activité anormaux, tels que la création massive de tâches planifiées ou une augmentation soudaine du trafic C2.

---
[Source](https://isc.sans.edu/diary/rss/32628){:target="_blank"}
