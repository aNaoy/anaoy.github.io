---
title: 'New Mistic Backdoor Linked to KongTuke in ClickFix and ModeloRAT Campaigns'
date: 2026-06-25
permalink: /posts/2026/06/25/new-mistic-backdoor-linked-to-kongtuke-in-clickfix-and-modelorat-campaigns/
tags:
- veille-cyber
- hackernews
---
### Mistic : Une nouvelle porte dérobée furtive au cœur des campagnes KongTuke

Le groupe cybercriminel **KongTuke** (également connu sous les noms de 404 TDS ou Woodgnat) déploie une nouvelle porte dérobée baptisée **Mistic** (ou MLTBackdoor). Ce malware, souvent associé au cheval de Troie d'accès à distance (**ModeloRAT**), est utilisé pour établir un accès persistant et discret chez des cibles variées (assurance, éducation, services IT).

**Points clés :**
*   **Mode opératoire :** Utilisation de campagnes « ClickFix » (tromperie d'utilisateurs via de faux messages d'erreur ou extensions de navigateur), de sites WordPress compromis et de messages frauduleux sur Microsoft Teams.
*   **Furtivité :** Mistic fonctionne entièrement en mémoire (fileless), ne laissant aucune trace sur le disque dur. Il utilise le *DLL side-loading* en détournant l'exécutable légitime de Microsoft (`MpExtMs.exe`) pour éviter toute détection.
*   **Objectif :** Accès initial pour revente ultérieure à des groupes de ransomware, comme observé avec le déploiement de Qilin.

**Capacités du malware :**
*   Exécution de code et de fichiers (BOF) directement en mémoire.
*   Gestion complète de fichiers (téléchargement, déplacement, suppression).
*   Communication C2 personnalisable et fonction d'auto-suppression (kill switch).

**Vulnérabilités :**
*   L'article ne mentionne pas de CVE spécifique, car les attaques reposent sur l'ingénierie sociale (ClickFix) et le détournement de processus légitimes par *DLL side-loading* plutôt que sur l'exploitation directe d'une faille logicielle.

**Recommandations :**
*   **Sensibilisation :** Former les utilisateurs à la méfiance face aux fenêtres contextuelles de navigateur demandant l'exécution de scripts ou l'installation d'extensions non approuvées.
*   **Surveillance réseau :** Surveiller les requêtes DNS inhabituelles, souvent utilisées comme canal de signalement ou de récupération de charges utiles par ce groupe.
*   **Sécurité des terminaux :** Renforcer les politiques EDR pour détecter le *DLL side-loading* et les comportements suspects émanant de processus systèmes normalement de confiance.
*   **Filtrage :** Restreindre les communications sortantes vers des domaines inconnus ou suspects, souvent gérés via les systèmes de distribution de trafic (TDS) de l'attaquant.

---
[Source](https://thehackernews.com/2026/06/new-mistic-backdoor-linked-to-kongtuke.html){:target="_blank"}
