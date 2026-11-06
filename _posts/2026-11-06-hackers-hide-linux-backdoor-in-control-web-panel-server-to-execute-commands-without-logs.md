---
title: 'Hackers Hide Linux Backdoor in Control Web Panel Server to Execute Commands Without Logs'
date: 2026-11-06
permalink: /posts/2026/11/06/hackers-hide-linux-backdoor-in-control-web-panel-server-to-execute-commands-without-logs/
tags:
- veille-cyber
- hackernews
---
### Découverte de "cwpdoor" : une porte dérobée invisible dans Control Web Panel

Une porte dérobée baptisée **cwpdoor** a été identifiée au sein du serveur web `cwpsrv` utilisé par Control Web Panel (CWP). Ce malware permet l'exécution de commandes distantes sans laisser de traces dans les journaux d'accès.

**Points clés :**
*   **Mode opératoire :** Le malware remplace le binaire légitime `cwpsrv` par une version modifiée. Il intercepte des requêtes web contenant des en-têtes personnalisés spécifiques (`X-Ngx-Integrity`) pour déclencher l'exécution de commandes.
*   **Persistance :** L'installateur falsifie les horodatages des fichiers modifiés pour éviter la détection par les commandes classiques (`ls`, `stat`).
*   **Vecteur d'infection :** L'installation nécessite un accès root préalable, bien que la méthode d'obtention de cet accès reste inconnue.
*   **Impact :** Des preuves d'utilisation réelle ont été détectées (VirusTotal, Brésil), compromettant potentiellement l'intégrité totale des serveurs touchés.

**Vulnérabilités :**
*   Aucune CVE spécifique n'est associée, car il s'agit d'une altération malveillante du binaire `cwpsrv` (versions 1.15.10 et 1.24.0). Le malware tire parti d'un accès root déjà acquis pour compromettre le serveur.

**Recommandations :**
*   **Vérification :**
    *   Exécuter `ss -axp | grep integrity` : la présence de `ngx_http_integrity_helper` indique une infection.
    *   Exécuter `strings /usr/local/cwpsrv/bin/cwpsrv | grep X-Ngx-Integrity` pour détecter la présence des en-têtes malveillants.
*   **Remédiation :**
    *   Restaurer le binaire `cwpsrv` original à partir d'une sauvegarde saine.
    *   Mettre à jour CWP vers la version la plus récente.
    *   Réinitialiser tous les mots de passe et identifiants du panneau de contrôle.
    *   Considérer le serveur comme totalement compromis et procéder à une investigation approfondie pour détecter d'autres menaces (le malware ayant été trouvé associé au botnet Ebury).

---
[Source](https://thehackernews.com/2026/11/hackers-hide-linux-backdoor-in-control.html){:target="_blank"}
