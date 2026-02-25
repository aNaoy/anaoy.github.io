---
title: 'Chinese cyberspies breached dozens of telecom firms, govt agencies'
date: 2026-02-25
permalink: /posts/2026/02/25/chinese-cyberspies-breached-dozens-of-telecom-firms-govt-agencies/
tags:
- veille-cyber
- bleepingcomp
---
### Campagne d'espionnage mondial utilisant des API pour dissimuler le trafic

Une campagne d'espionnage mondiale, attribuée à un acteur malveillant chinois présumé, a ciblé 53 organisations dans 42 pays, affectant des entreprises de télécommunications et des agences gouvernementales. Active depuis au moins 2023, cette opération utilise des appels aux API de services SaaS pour masquer le trafic malveillant.

L'accès initial reste inconnu, mais l'acteur, connu sous le nom de UNC2814, a historiquement exploité des failles dans les serveurs web et les systèmes périphériques.

Le groupe malveillant a déployé une nouvelle porte dérobée écrite en C, nommée GRIDTIDE. Celle-ci abuse de l'API Google Sheets pour ses opérations de commande et contrôle (C2). GRIDTIDE utilise un compte de service Google avec une clé privée codée en dur pour s'authentifier. Après son exécution, elle nettoie la feuille de calcul en supprimant les premières lignes et colonnes. Elle collecte ensuite des informations sur le système cible (nom d'utilisateur, nom d'hôte, détails du système d'exploitation, IP locale, localisation, fuseau horaire) et enregistre ces données dans une cellule spécifique de la feuille. La cellule A1 sert de canal pour les commandes et les statuts, GRIDTIDE interrogeant cette cellule pour recevoir des instructions. Les commandes supportées permettent l'exécution de scripts bash encodés en Base64, le téléversement et le téléchargement de fichiers. Les échanges avec le C2 sont encodés en Base64 compatible URL, ce qui permet d'éviter la détection par les outils de surveillance web.

Bien que l'exfiltration de données n'ait pas été directement observée, un cas a révélé le déploiement de GRIDTIDE sur un système contenant des informations personnelles identifiables (PII) sensibles.

Google, Mandiant et leurs partenaires ont mené une action coordonnée pour perturber cette campagne, notamment en résiliant les projets cloud de UNC2814, en désactivant l'infrastructure connue, en révoquant l'accès aux API Google Sheets et en détournant des domaines. Les organisations touchées ont été informées et ont reçu de l'aide pour nettoyer les infections.

Il est anticipé que UNC2814 reprendra ses activités avec de nouvelles infrastructures prochainement.

**Points Clés :**
*   Campagne d'espionnage mondial ciblant les télécommunications et les gouvernements.
*   Utilisation d'API (Google Sheets) pour dissimuler le trafic C2.
*   Déploiement d'une nouvelle porte dérobée : GRIDTIDE.
*   Collecte d'informations système et exécution de commandes à distance.
*   Action de disruption coordonnée par Google et partenaires.

**Vulnérabilités :**
*   Les détails spécifiques des vulnérabilités exploitées pour l'accès initial ne sont pas précisés dans l'article. L'article mentionne que l'acteur a précédemment gagné l'accès en exploitant des failles dans les serveurs web et les systèmes périphériques.
*   Aucun numéro CVE n'est mentionné dans l'article.

**Recommandations :**
*   Les organisations impactées ont été directement notifiées et ont reçu de l'aide pour éradiquer les infections.
*   Google a publié des règles de détection et des indicateurs de compromission (IoCs) pour aider à identifier et contrer les menaces.
*   Il est conseillé aux organisations de rester vigilantes face à la reprise potentielle des activités par l'acteur UNC2814 avec de nouvelles infrastructures.

---
[Source](https://www.bleepingcomputer.com/news/security/chinese-cyberspies-breached-dozens-of-telecom-firms-govt-agencies/){:target="_blank"}
