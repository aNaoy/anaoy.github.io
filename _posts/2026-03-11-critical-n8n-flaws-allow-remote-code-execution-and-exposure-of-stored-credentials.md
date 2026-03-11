---
title: 'Critical n8n Flaws Allow Remote Code Execution and Exposure of Stored Credentials'
date: 2026-03-11
permalink: /posts/2026/03/11/critical-n8n-flaws-allow-remote-code-execution-and-exposure-of-stored-credentials/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques et exécution de code à distance dans n8n

La plateforme d'automatisation n8n a corrigé plusieurs vulnérabilités critiques permettant l'exécution de code à distance (RCE) et l'exposition d'identifiants stockés. Ces failles concernent les déploiements auto-hébergés et Cloud.

**Points clés :**
*   Les vulnérabilités permettent à des attaquants de compromettre le serveur hôte et d'accéder à des secrets sensibles (clés AWS, jetons OAuth, mots de passe) via la clé de chiffrement `N8N_ENCRYPTION_KEY`.
*   Certaines failles (ex: `CVE-2026-27493`) ne nécessitent aucune authentification, exploitant les formulaires publics pour injecter des commandes.

**Vulnérabilités identifiées :**
*   **CVE-2026-27577 (CVSS 9.4) :** Évasion du bac à sable (sandbox) de l'expression compiler menant à une exécution de code à distance.
*   **CVE-2026-27493 (CVSS 9.5) :** Problème de double évaluation dans les nœuds de formulaire, permettant une injection d'expression sans authentification.
*   **CVE-2026-27495 (CVSS 9.4) :** Injection de code dans le bac à sable du "JavaScript Task Runner" par un utilisateur authentifié.
*   **CVE-2026-27497 (CVSS 9.4) :** Injection de code et écriture de fichiers arbitraires via le mode SQL du nœud "Merge".

**Recommandations :**
*   **Mise à jour immédiate :** Passer aux versions **2.10.1, 2.9.3 ou 1.123.22**, qui corrigent l'ensemble de ces failles.
*   **Mitigations temporaires (si la mise à jour est impossible) :**
    *   **Nœuds de formulaire :** Désactiver les nœuds `Form` et `Form Trigger` via la variable d'environnement `NODES_EXCLUDE` (`n8n-nodes-base.form`, `n8n-nodes-base.formTrigger`).
    *   **Nœud Merge :** Désactiver via `n8n-nodes-base.merge`.
    *   **JavaScript Task Runner :** Utiliser le mode externe (`N8N_RUNNERS_MODE=external`) pour limiter l'impact.
    *   **Sécurisation générale :** Restreindre les permissions de création/modification de workflows aux seuls utilisateurs de confiance et durcir l'environnement d'exécution (privilèges OS et accès réseau limités).

---
[Source](https://thehackernews.com/2026/03/critical-n8n-flaws-allow-remote-code.html){:target="_blank"}
