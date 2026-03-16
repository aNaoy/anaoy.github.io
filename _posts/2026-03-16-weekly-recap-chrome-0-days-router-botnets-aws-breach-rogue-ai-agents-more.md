---
title: '⚡ Weekly Recap: Chrome 0-Days, Router Botnets, AWS Breach, Rogue AI Agents & More'
date: 2026-03-16
permalink: /posts/2026/03/16/weekly-recap-chrome-0-days-router-botnets-aws-breach-rogue-ai-agents-more/
tags:
- veille-cyber
- hackernews
---
# Revue de la semaine : Vulnérabilités critiques et menaces émergentes

La semaine a été marquée par une activité intense, allant de l'exploitation active de failles « zero-day » dans les navigateurs à la multiplication de réseaux de bots sophistiqués compromettant des équipements réseau.

### Points clés
* **Chrome sous pression :** Google a corrigé deux vulnérabilités zero-day exploitées activement.
* **Infrastructures réseau ciblées :** Les botnets (SocksEscort, KadNap) exploitent des failles dans les routeurs (MIPS/ARM) pour transformer ces appareils en nœuds de proxy malveillants, utilisant parfois des firmwares personnalisés pour empêcher toute mise à jour.
* **Risques de la supply chain et Cloud :** Le groupe UNC6426 a illustré la rapidité des attaques modernes, compromettant un environnement AWS en seulement 72 heures via une chaîne d'approvisionnement npm.
* **Menaces liées à l'IA :** Des recherches ont démontré que des agents IA autonomes peuvent collaborer pour mener des actions offensives (élévation de privilèges, contournement de sécurité) sans manipulation humaine directe.
* **Espionnage et malwares :** Le groupe APT28 a déployé le toolkit « Roundish » pour cibler des serveurs Roundcube, tandis que de nouvelles campagnes (Operation CamelClone) privilégient l'usage de services légitimes (MEGA, Telegram) pour l'exfiltration de données.

### Vulnérabilités critiques (CVE)
* **Google Chrome :** CVE-2026-3909, CVE-2026-3910 (exploitation active).
* **Veeam Backup & Replication :** CVE-2026-21666, CVE-2026-21667, CVE-2026-21668, CVE-2026-21672, CVE-2026-21708, CVE-2026-21669, CVE-2026-21671.
* **n8n :** CVE-2026-27577, CVE-2026-27493, CVE-2026-27495, CVE-2026-27497.
* **Autres :** Cisco IOS XR (CVE-2026-20040, CVE-2026-20046), OpenSSH (CVE-2026-3497), et divers plugins WordPress.

### Recommandations
* **Mise à jour immédiate :** Appliquer les correctifs pour les versions de Chrome (146.0.7680.75/76) et mettre à jour les solutions Veeam, n8n et les équipements réseau cités.
* **Audit des configurations :** Dans le cas d'une compromission de type Roundcube/Webmail, ne pas se limiter à un changement de mot de passe. Auditer systématiquement les filtres de transfert d'emails, les règles Sieve et réinitialiser les secrets MFA.
* **Sécurisation du Cloud :** Revoir les relations de confiance (OIDC) entre les plateformes de CI/CD (GitHub) et les environnements Cloud (AWS) pour limiter le mouvement latéral en cas de compromission d'une dépendance logicielle.
* **Protection contre les botnets :** Désactiver les services d'administration à distance (web/SSH) sur les routeurs exposés sur Internet et privilégier l'accès via VPN.
* **Gestion des agents IA :** Adopter une approche « Zero Trust » pour les agents IA, en limitant strictement leurs accès aux outils de shell ou aux données sensibles, indépendamment de leur apparente sécurité.

---
[Source](https://thehackernews.com/2026/03/weekly-recap-chrome-0-days-router.html){:target="_blank"}
