---
title: 'New EDR killer tool used by eight different ransomware groups'
date: 2025-08-07
permalink: /posts/2025/08/07/new-edr-killer-tool-used-by-eight-different-ransomware-groups/
tags:
- veille-cyber
- bleepingcomp
---
**L'Évolution des Outils d'Évasion des EDR : Une Menace Partagée**

Une nouvelle génération d'outils conçus pour neutraliser les solutions de détection et de réponse sur les points d'extrémité (EDR) a été identifiée, succédant à des malwares tels que 'EDRKillShifter'. Ce type d'outil permet aux acteurs de la menace de désactiver les logiciels de sécurité sur les systèmes compromis, facilitant ainsi le déploiement de charges utiles malveillantes, l'escalade de privilèges, les mouvements latéraux et le chiffrement des données sans être détectés.

Ce nouvel outil, utilisé par huit groupes de ransomware distincts, y compris RansomHub, Blacksuit, Medusa, Qilin, Dragonforce, Crytox, Lynx et INC, présente une architecture complexe. Il utilise un binaire fortement obfusqué qui se décode à l'exécution et s'injecte dans des applications légitimes. La technique clé repose sur la recherche et l'exploitation d'un pilote signé numériquement (via un certificat volé ou expiré) pour exécuter une attaque de type "Bring Your Own Vulnerable Driver" (BYOVD). Ce pilote s'insère dans le noyau du système, obtenant les privilèges nécessaires pour arrêter les processus et les services des logiciels de sécurité.

Les produits de sécurité ciblés incluent une large gamme de solutions de confiance telles que Sophos, Microsoft Defender, Kaspersky, Symantec, Trend Micro, SentinelOne, Cylance, McAfee, F-Secure, HitmanPro et Webroot. Bien que les variantes de cet outil présentent des différences au niveau des noms de pilotes, des antivirus visés et des caractéristiques de compilation, elles partagent une utilisation commune de HeartCrypt pour le packing et suggèrent un partage de connaissances et d'outils entre différents groupes de menaces. Il est probable que cet outil ne soit pas le résultat d'une fuite unique, mais plutôt d'un cadre de développement collaboratif.

Ce partage de tactiques et d'outils, en particulier pour les désactiveurs d'EDR, n'est pas nouveau dans l'écosystème des ransomwares. Des exemples antérieurs incluent 'AuKill' utilisé par Medusa Locker et LockBit, ainsi que 'AvNeutralizer' vendu par FIN7 à divers gangs de ransomware.

**Points Clés :**

*   Apparition d'un nouvel outil sophistiqué pour désactiver les EDR.
*   Utilisé par au moins huit groupes de ransomware différents.
*   Technique principale : "Bring Your Own Vulnerable Driver" (BYOVD) via un pilote signé numériquement.
*   Cible un large éventail de solutions de sécurité EDR/AV.
*   Preuves de partage de connaissances et d'outils entre groupes de menaces concurrents.

**Vulnérabilités :**

*   Pas de CVE spécifiques mentionnées dans l'article, mais la vulnérabilité exploitée est celle permettant le chargement de pilotes non signés ou malveillants dans le noyau (concept BYOVD).

**Recommandations :**

*   Mettre à jour les systèmes et les solutions de sécurité pour se prémunir contre les vulnérabilités BYOVD connues.
*   Surveiller et détecter les activités suspectes liées au chargement de pilotes inhabituels.
*   Maintenir une vigilance constante et une bonne hygiène de sécurité des points d'extrémité.

---
[Source](https://www.bleepingcomputer.com/news/security/new-edr-killer-tool-used-by-eight-different-ransomware-groups/){:target="_blank"}
