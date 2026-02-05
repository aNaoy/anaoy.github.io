---
title: 'Hackers compromise NGINX servers to redirect user traffic'
date: 2026-02-05
permalink: /posts/2026/02/05/hackers-compromise-nginx-servers-to-redirect-user-traffic/
tags:
- veille-cyber
- bleepingcomp
---
**Campagne de détournement de trafic via des serveurs NGINX compromis**

Une campagne de cyberattaques active vise des serveurs utilisant NGINX et le panneau de gestion d'hébergement Baota. Les attaquants modifient les fichiers de configuration NGINX pour intercepter le trafic des utilisateurs et le rediriger vers leur propre infrastructure, imitant ainsi les fonctionnalités légitimes de routage du trafic.

**Points clés :**

*   Les attaquants injectent des blocs de configuration `location` malveillants dans les fichiers de configuration NGINX.
*   Ces blocs capturent les requêtes entrantes sur des chemins d'URL spécifiques choisis par l'attaquant.
*   Les requêtes sont ensuite réécrites pour inclure l'URL d'origine complète et transmises à des domaines contrôlés par les attaquants via la directive `proxy_pass`.
*   Les en-têtes de requête tels que `Host`, `X-Real-IP`, `User-Agent` et `Referer` sont conservés pour masquer l'activité malveillante.
*   L'attaque utilise un kit d'outils en cinq étapes (`zx.sh`, `bt.sh`, `4zdh.sh`, `zdh.sh`, `ok.sh`) pour automatiser le processus d'injection et d'exfiltration des données.
*   Les cibles privilégiées semblent être les sites utilisant des domaines de premier niveau asiatiques (.in, .id, .pe, .bd, .th) ainsi que les sites gouvernementaux et éducatifs (.edu, .gov).
*   La difficulté de détection réside dans le fait que l'attaque ne repose pas sur une vulnérabilité NGINX exploitée, mais sur la modification des fichiers de configuration, qui sont rarement examinés de près. De plus, le trafic atteint toujours la destination prévue, rendant le passage par l'infrastructure de l'attaquant difficile à remarquer sans une surveillance spécifique.

**Vulnérabilités :**

*   Aucune vulnérabilité NGINX spécifique (CVE) n'est mentionnée dans l'article. L'attaque exploite la modification des fichiers de configuration.

**Recommandations :**

*   Surveiller attentivement les fichiers de configuration NGINX pour détecter toute modification suspecte ou injection de blocs `location` non autorisés.
*   Mettre en place des mécanismes de détection d'altération des fichiers de configuration critiques.
*   Examiner régulièrement les journaux de NGINX pour identifier des schémas de trafic inhabituels ou des redirections inattendues, bien que l'attaque soit conçue pour minimiser la détection.
*   Sécuriser l'accès aux panneaux de gestion d'hébergement tels que Baota, qui peuvent servir de point d'entrée initial ou de levier pour la modification des configurations.

---
[Source](https://www.bleepingcomputer.com/news/security/hackers-compromise-nginx-servers-to-redirect-user-traffic/){:target="_blank"}
