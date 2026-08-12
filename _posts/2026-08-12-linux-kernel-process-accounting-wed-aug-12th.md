---
title: 'Linux Kernel Process Accounting, (Wed, Aug 12th)'
date: 2026-08-12
permalink: /posts/2026/08/12/linux-kernel-process-accounting-wed-aug-12th/
tags:
- veille-cyber
- sans-isc
---
### Surveillance de l'activité système avec le processus comptable Linux

La comptabilité des processus Linux est une fonctionnalité native du noyau permettant d'enregistrer l'exécution des processus de manière exhaustive. Contrairement aux historiques de shell (type `.bash_history`), cette méthode capture toutes les activités, y compris celles des processus non interactifs ou lancés par des scripts.

**Points clés :**
*   **Fonctionnement :** Une fois activée via la commande `accton`, le noyau écrit des données binaires sur chaque processus terminé dans `/var/log/account/pacct`.
*   **Données enregistrées :** Nom du processus, privilèges (super-utilisateur), indicateurs (fork, dump), temps CPU et horodatage.
*   **Analyse :** Les outils `lastcomm` (lecture des logs) et `sa` (résumé statistique) permettent une exploitation simple des données.
*   **Centralisation :** Bien que non natif via syslog, il est possible d'utiliser des collecteurs comme `syslog-ng` pour envoyer ces logs vers un SIEM.
*   **Conteneurs :** Sur un hôte, les processus des conteneurs sont enregistrés directement par le noyau de l'hôte, offrant une meilleure intégrité des logs en cas de compromission du conteneur.

**Vulnérabilités :**
*   Aucune CVE spécifique associée. 
*   **Limitation critique :** Cette fonctionnalité n'enregistre pas les arguments de ligne de commande, ce qui peut freiner l'analyse forensique détaillée lors d'une réponse à incident.

**Recommandations :**
*   **Déploiement :** Installer le paquet `acct` (Debian/Ubuntu) et activer le service (`systemctl enable --now acct`).
*   **Sécurité :** Utiliser la comptabilité des processus comme une couche de sécurité complémentaire aux logs d'audit (auditd) et aux historiques shell.
*   **Intégrité :** Pour les environnements conteneurisés, privilégier la collecte au niveau de l'hôte plutôt que dans le conteneur afin d'empêcher toute altération des logs par un attaquant.
*   **Alternative :** Pour des besoins d'inspection plus granulaires (notamment pour capturer les arguments), envisager l'utilisation d'eBPF.

---
[Source](https://isc.sans.edu/diary/rss/33240){:target="_blank"}
