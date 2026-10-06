---
title: 'Critical Atlassian Flaw Lets Unauthenticated Attackers Read Known Files Across 8 Products'
date: 2026-10-06
permalink: /posts/2026/10/06/critical-atlassian-flaw-lets-unauthenticated-attackers-read-known-files-across-8-products/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique de lecture de fichiers dans les produits Atlassian

Une faille de sécurité critique, identifiée comme **CVE-2026-21589** (score CVSS 9.3), affecte huit produits Atlassian en version "Data Center" auto-hébergés. Cette vulnérabilité de type *path traversal* permet à un attaquant non authentifié de lire des fichiers spécifiques situés dans le répertoire racine de l'application web, à condition de connaître le nom exact et le chemin du fichier visé.

**Points clés :**
*   **Impact :** Accès en lecture non autorisé à des fichiers potentiellement sensibles sur le serveur.
*   **Produits concernés :** Bitbucket, Confluence, Jira Software, Jira Service Management, Bamboo, Crowd, Crucible et Fisheye.
*   **Gravité :** Élevée (9.3/10), l'exploitation ne nécessite ni authentification ni interaction utilisateur.
*   **Statut :** Les solutions cloud d'Atlassian sont déjà corrigées. Les versions "Server" (anciennes) sont également mentionnées comme potentiellement vulnérables, sans correctifs clairs pour certaines d'entre elles.

**Recommandations :**
1.  **Mise à jour immédiate :** Appliquer les correctifs vers les versions listées comme sécurisées pour chaque produit.
2.  **Mesures de contournement :** Si la mise à jour est impossible à court terme, restreindre l'accès réseau public (placer l'instance hors ligne) ou mettre en place des règles de blocage (via WAF, reverse proxy ou configurations spécifiques comme *Tomcat RewriteValve* ou *urlrewrite.xml*) pour interdire les chaînes malveillantes contenant `..` suivies de `/`, `\` ou `::`.
3.  **Audit des logs :** Analyser les journaux d'accès à la recherche de tentatives d'exploitation utilisant des séquences de *path traversal* (encodées ou non).
4.  **Vérification :** Bien que l'exploitation n'ait pas été confirmée, Atlassian recommande une vigilance accrue, l'historique montrant que ce type de faille (ex: CVE-2021-26086) est activement ciblé par les attaquants.

---
[Source](https://thehackernews.com/2026/10/critical-atlassian-flaw-lets.html){:target="_blank"}
