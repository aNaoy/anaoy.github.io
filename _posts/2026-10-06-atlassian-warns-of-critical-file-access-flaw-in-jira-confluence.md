---
title: 'Atlassian warns of critical file-access flaw in Jira, Confluence'
date: 2026-10-06
permalink: /posts/2026/10/06/atlassian-warns-of-critical-file-access-flaw-in-jira-confluence/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilité critique d'accès aux fichiers dans les produits Atlassian

Atlassian a émis une alerte concernant une vulnérabilité critique affectant ses solutions auto-hébergées (Data Center), permettant à un attaquant non authentifié d'accéder à des fichiers spécifiques situés dans le répertoire racine web de l'application.

**Points clés :**
*   **Impact :** Accès arbitraire à des fichiers sensibles.
*   **Condition d'exploitation :** L'attaquant doit connaître le nom exact et le chemin d'accès du fichier cible (pas d'énumération de répertoire possible).
*   **Produits concernés :** Jira (Software et Service Management), Confluence, Bitbucket, Bamboo, Crowd, Crucible et Fisheye.
*   **Statut :** Aucune preuve d'exploitation active n'a été constatée à ce jour, mais les administrateurs sont invités à vérifier leurs journaux d'accès.

**Vulnérabilité identifiée :**
*   **CVE-2026-21589**

**Recommandations :**
*   **Mise à jour immédiate :** Installer les correctifs fournis par Atlassian pour chaque produit (les versions corrigées sont listées dans l'avis de sécurité officiel).
*   **Instances Cloud :** Aucune action requise, le déploiement des correctifs est automatique.
*   **Atténuations temporaires :** 
    *   Restreindre l'accès réseau externe des instances.
    *   Configurer un WAF (Web Application Firewall) ou des règles de proxy pour bloquer les patterns de traversée de répertoires.
    *   Appliquer des règles spécifiques (Tomcat RewriteValve ou URL rewrite) selon le produit utilisé.
*   **Vérification :** Auditer les journaux d'accès à la recherche de tentatives de traversée suspectes et consulter les équipes de sécurité locales en cas de doute sur une compromission.

---
[Source](https://www.bleepingcomputer.com/news/security/atlassian-warns-of-critical-file-access-flaw-in-jira-confluence/){:target="_blank"}
