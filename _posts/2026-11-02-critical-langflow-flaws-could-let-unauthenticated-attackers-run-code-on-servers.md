---
title: 'Critical Langflow Flaws Could Let Unauthenticated Attackers Run Code on Servers'
date: 2026-11-02
permalink: /posts/2026/11/02/critical-langflow-flaws-could-let-unauthenticated-attackers-run-code-on-servers/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans Langflow : Risques d'exécution de code à distance

Langflow, un outil open-source destiné à la création d'agents IA, est exposé à plusieurs vulnérabilités critiques permettant à des attaquants non authentifiés de contourner la sécurité ou d'exécuter du code arbitraire sur les serveurs. L'ensemble des versions comprises entre la 1.0.0 et la 1.12.8 est impacté.

**Points clés :**
*   **Risque majeur :** La configuration par défaut `LANGFLOW_AUTO_LOGIN`, activée jusqu'à la version 1.12.8, connecte automatiquement les utilisateurs en tant que superutilisateurs, facilitant les accès non autorisés.
*   **Exploitation :** Un module Metasploit existe déjà pour exploiter la vulnérabilité de contournement d'authentification (CVE-2026-93680).
*   **Extension de la menace :** Au total, 33 vulnérabilités ont été identifiées récemment, incluant d'autres failles critiques (ex: CVE-2026-104339).

**Vulnérabilités principales :**
*   **CVE-2026-93680 (CVSS 9.8) :** Contournement de l'authentification (aucun compte requis).
*   **CVE-2026-110186 (CVSS 9.8) :** Exécution de code arbitraire via un contrôle défaillant de la génération de code (aucun compte requis).
*   **CVE-2026-110193 (CVSS 8.8) :** Injection de commandes système via l'Assistant Agentique (compte à faible privilège requis).
*   **CVE-2026-110192 (CVSS 6.5) :** Exfiltration d'informations sensibles liées aux identifiants (compte requis).

**Recommandations :**
*   **Mise à jour immédiate :** Passer impérativement à la version **1.13.0**, qui désactive l'auto-connexion par défaut et corrige les failles citées.
*   **Procédure de migration :**
    1. Sauvegarder la base de données, la clé secrète et les fichiers téléchargés avant toute opération.
    2. Si l'auto-connexion est active, préparer un accès par mot de passe pour le compte utilisateur.
    3. Mettre à jour le package via `pip install --upgrade "langflow==1.13.0"` ou via l'image Docker appropriée.
    4. Ne pas réinstaller ou supprimer l'application pour éviter la perte permanente des flux (flows) de données.

---
[Source](https://thehackernews.com/2026/11/critical-langflow-flaws-could-let.html){:target="_blank"}
