---
title: 'New Fragnesia Linux Kernel LPE Grants Root Access via Page Cache Corruption'
date: 2026-05-14
permalink: /posts/2026/05/14/new-fragnesia-linux-kernel-lpe-grants-root-access-via-page-cache-corruption/
tags:
- veille-cyber
- hackernews
---
### Fragnesia : Une nouvelle vulnérabilité critique d'escalade de privilèges sous Linux

Une nouvelle faille de sécurité baptisée **Fragnesia** a été identifiée dans le noyau Linux. Cette vulnérabilité permet à un utilisateur local non privilégié d'obtenir un accès root en corrompant le cache de page du noyau, ciblant spécifiquement le sous-système XFRM ESP-in-TCP.

**Points clés :**
*   **Nature de la faille :** Contrairement aux attaques basées sur des conditions de concurrence (*race conditions*), Fragnesia exploite un défaut logique permettant l'écriture arbitraire d'octets dans le cache de page de fichiers en lecture seule.
*   **Impact :** L'exploit permet une élévation de privilèges (LPE) immédiate et stable, similaire aux vulnérabilités *Dirty Frag* et *Copy Fail*.
*   **Disponibilité :** Un code d'exploitation (PoC) a été rendu public par l'équipe de recherche V12.
*   **Contexte :** Il s'agit de la troisième vulnérabilité majeure découverte dans le noyau Linux en deux semaines, dans un contexte où des exploits zero-day sont activement commercialisés sur des forums cybercriminels.

**Détails de la vulnérabilité :**
*   **Identifiant :** CVE-2026-46300
*   **Score CVSS :** 7.8 (Élevé)

**Recommandations :**
*   **Mise à jour :** Appliquer les correctifs de sécurité dès que possible via les outils de mise à jour des distributions concernées (Debian, Ubuntu, Red Hat, SUSE, etc.).
*   **Atténuation immédiate :** Si le déploiement du patch est impossible, appliquer les mesures préventives utilisées pour *Dirty Frag* :
    *   Désactiver les modules `esp4`, `esp6` et les fonctionnalités `xfrm`/`IPsec` inutilisées.
    *   Restreindre l'accès local au shell.
    *   Renforcer la sécurité des conteneurs.
    *   Surveiller les activités anormales liées à l'escalade de privilèges.
*   **Sécurité complémentaire :** L'utilisation de restrictions AppArmor sur les espaces de noms utilisateur (*user namespaces*) peut servir de mesure d'atténuation partielle.

---
[Source](https://thehackernews.com/2026/05/new-fragnesia-linux-kernel-lpe-grants.html){:target="_blank"}
