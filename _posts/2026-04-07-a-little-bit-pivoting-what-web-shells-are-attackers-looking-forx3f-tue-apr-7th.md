---
title: 'A Little Bit Pivoting: What Web Shells are Attackers Looking for&#x3f;, (Tue, Apr 7th)'
date: 2026-04-07
permalink: /posts/2026/04/07/a-little-bit-pivoting-what-web-shells-are-attackers-looking-forx3f-tue-apr-7th/
tags:
- veille-cyber
- sans-isc
---
### Analyse des tactiques d'injection de Web Shells

Les attaquants utilisent couramment des « web shells » pour maintenir une persistance sur des serveurs compromis, en exploitant des vulnérabilités d'exécution de code à distance (RCE) ou d'écriture arbitraire de fichiers. Une analyse récente du trafic malveillant révèle que les attaquants privilégient des noms de fichiers discrets, imitant souvent la structure de répertoires de systèmes comme WordPress (ex: `/wp-content/`) pour se fondre dans la masse. Certaines de ces charges utiles intègrent des identifiants par défaut faibles, facilitant l'accès aux acteurs tiers.

**Points clés :**
*   **Dissimulation :** Les attaquants renomment constamment leurs web shells pour paraître légitimes.
*   **Techniques de reconnaissance :** L'analyse des cibles montre une utilisation intensive de techniques de *fingerprinting* (empreinte numérique) via l'exploration de chemins de fichiers spécifiques pour identifier les vulnérabilités exploitables.
*   **Infrastructure :** Le trafic observé provenait d'adresses IP liées à des environnements cloud (Microsoft), suggérant soit une compromission d'infrastructure légitime, soit une cible interne au cloud.
*   **Inutilité des listes noires :** Se baser sur une liste de noms de fichiers pour détecter les web shells est inefficace en raison de la trop grande variété des noms utilisés et des risques élevés de faux positifs.

**Vulnérabilités associées :**
*   **RCE (Remote Code Execution) :** Permet l'exécution de commandes système.
*   **Arbitrary File Upload/Write :** Permet l'injection de scripts malveillants sur le serveur.
*   *Note : Bien que l'article n'énumère pas de CVE spécifiques, ces vecteurs d'attaque sont généralement liés à des vulnérabilités non corrigées dans les plugins CMS, les thèmes ou les composants serveurs.*

**Recommandations de sécurité :**
*   **Durcissement des permissions :** Restreindre strictement les droits en écriture dans la racine du document (document root) pour empêcher le dépôt de fichiers non autorisés.
*   **Surveillance proactive :** Mettre en place un système d'intégrité des fichiers permettant de détecter toute modification non planifiée ou l'ajout de nouveaux scripts sur le serveur.
*   **Gestion des vulnérabilités :** Maintenir les CMS et leurs extensions à jour pour limiter les risques de RCE et d'upload arbitraire.

---
[Source](https://isc.sans.edu/diary/rss/32874){:target="_blank"}
