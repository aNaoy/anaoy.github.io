---
title: 'ShinyHunters hacked Clop leak site using Grav CMS path traversal flaw'
date: 2026-09-26
permalink: /posts/2026/09/26/shinyhunters-hacked-clop-leak-site-using-grav-cms-path-traversal-flaw/
tags:
- veille-cyber
- bleepingcomp
---
### Piratage du site de fuite de données du gang Clop

Le groupe de cybercriminels ShinyHunters a réussi à compromettre le site de fuite de données du gang de rançongiciel Clop en exploitant une faille critique de type « path traversal » (traversée de chemin) au sein du CMS Grav.

**Points clés :**
*   **Intrusion :** ShinyHunters a pris le contrôle du site de Clop, y affichant son propre logo et menaçant d'exposer des données volées.
*   **Données compromises :** ShinyHunters affirme avoir dérobé du code source, des logs serveurs et des clés privées Tor. Clop minimise l'incident en assurant que le serveur ne contenait aucune donnée sensible.
*   **Réaction :** Le gang Clop a migré vers une nouvelle adresse onion, confirmant que son installation Grav n'était pas à jour au moment des faits.

**Vulnérabilités :**
*   **CVE-2026-42608 :** Une faille de traversée de chemin située dans le cœur du CMS Grav. Elle permet à un attaquant non authentifié d'écrire des fichiers arbitraires sur le serveur en manipulant les paramètres de téléchargement de formulaires (via le paramètre `__unique_form_id__`).

**Recommandations :**
*   **Mise à jour urgente :** Les utilisateurs de la branche Grav 1.7 doivent impérativement mettre à jour leur installation vers la version **1.7.53.4**, qui inclut le correctif rétroporté.
*   **Migration vers Grav 2.x :** Les utilisateurs sont invités à migrer vers la version 2.0 ou supérieure, qui protège nativement contre cette vulnérabilité grâce à une fonction de nettoyage (`sanitizeId()`) des identifiants de formulaires.

---
[Source](https://www.bleepingcomputer.com/news/security/shinyhunters-hacked-clop-leak-site-using-grav-cms-path-traversal-flaw/){:target="_blank"}
