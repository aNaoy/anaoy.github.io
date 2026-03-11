---
title: 'Critical n8n Flaws Allow Remote Code Execution and Exposure of Stored Credentials'
date: 2026-03-11
permalink: /posts/2026/03/11/critical-n8n-flaws-allow-remote-code-execution-and-exposure-of-stored-credentials/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques et exécution de code à distance sur n8n

La plateforme d'automatisation de workflows **n8n** a corrigé plusieurs vulnérabilités critiques permettant l'exécution de code à distance (RCE) et l'exposition d'identifiants stockés, affectant les versions auto-hébergées et cloud.

**Points clés :**
*   **Impact :** Un attaquant peut obtenir un contrôle total du serveur, extraire la clé de chiffrement (`N8N_ENCRYPTION_KEY`) et déchiffrer tous les secrets stockés (clés AWS, OAuth, mots de passe).
*   **Vecteur d'attaque :** Certaines vulnérabilités sont exploitables sans authentification (via les formulaires publics), d'autres nécessitent des droits de création/modification de workflows.

**Vulnérabilités identifiées :**
*   **CVE-2026-27577 (CVSS 9.4) :** Échappement de la sandbox d'expressions permettant une RCE.
*   **CVE-2026-27493 (CVSS 9.5) :** Évaluation d'expression non authentifiée via les nœuds « Form ».
*   **CVE-2026-27495 (CVSS 9.4) :** Injection de code dans la sandbox du *Task Runner* JavaScript.
*   **CVE-2026-27497 (CVSS 9.4) :** Injection de code et écriture de fichiers arbitraires via le mode SQL du nœud « Merge ».

**Recommandations :**
*   **Mise à jour immédiate :** Passer aux versions **2.10.1, 2.9.3 ou 1.123.22**.
*   **Atténuations temporaires :**
    *   **Nœuds Form/FormTrigger :** Désactiver via la variable d'environnement `NODES_EXCLUDE` (`n8n-nodes-base.form`, `n8n-nodes-base.formTrigger`).
    *   **Nœud Merge :** Désactiver via `n8n-nodes-base.merge`.
    *   **Task Runner :** Utiliser le mode externe (`N8N_RUNNERS_MODE=external`).
    *   **Gestion des accès :** Restreindre la création/modification de workflows aux utilisateurs de confiance et durcir l'environnement d'exécution (privilèges OS limités, accès réseau restreint).

---
[Source](https://thehackernews.com/2026/03/critical-n8n-flaws-allow-remote-code.html){:target="_blank"}
