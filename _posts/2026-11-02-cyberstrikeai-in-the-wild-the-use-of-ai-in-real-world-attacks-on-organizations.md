---
title: 'CyberStrikeAI in the wild: the use of AI in real-world attacks on organizations'
date: 2026-11-02
permalink: /posts/2026/11/02/cyberstrikeai-in-the-wild-the-use-of-ai-in-real-world-attacks-on-organizations/
tags:
- veille-cyber
- securelist
---
### CyberStrikeAI : L’automatisation des cyberattaques par LLM

La campagne CyberStrikeAI marque une évolution majeure dans les cyberattaques en intégrant l’intelligence artificielle directement au cœur du processus de post-exploitation. Contrairement aux usages passés limités à la préparation (phishing, aide au code), un orchestrateur LLM sur le serveur de commande et contrôle (C2) planifie désormais les actions, sélectionne les outils et génère les commandes exécutées par des implants sur les systèmes compromis.

#### Points clés
*   **Mode opératoire :** L'attaquant humain définit une intention stratégique, tandis que le modèle d’IA choisit la séquence technique pour l'exécuter.
*   **Rapidité :** L’automatisation permet d’atteindre le compromis total d’un domaine en 3 à 4 jours, avec des phases de mouvement latéral et d'exfiltration s’exécutant en moins d'une heure.
*   **Architecture :** Le framework (développé en Go) sépare l’intelligence (serveur C2 avec LLM) de l’exécution (implant passif sans IA).
*   **Cibles :** Institutions éducatives en Afrique et en Amérique latine.

#### Vulnérabilités et vecteurs d'attaque
L'attaque n'exploite pas de vulnérabilités "Zero-day" liées à l'IA, mais combine des techniques classiques, facilitées par l'orchestration automatique :
*   **Vecteur initial :** Exploitation de serveurs SQL (ex: SQL Server 16.0.1000).
*   **Techniques utilisées :** 
    *   **Credential Access :** Dumping de mémoire `lsass.exe` via `comsvcs.dll` (MiniDump), Kerberoasting, AS-REP Roasting, et DCSync.
    *   **Persistance :** Tâches planifiées (`schtasks`), objets COM, clés de registre (`Run`) et cron jobs sous Linux.
    *   **Mouvement latéral :** Usage d'Impacket (`WMIExec`), WMI, PowerShell (`Invoke-CimMethod`) et partages réseau.
    *   **Élévation de privilèges :** Exploitation de `AlwaysInstallElevated` ou détournement de services.

#### Recommandations de défense
Bien que l'orchestration soit pilotée par une IA, les actions visibles sur le réseau et les hôtes restent classiques. La détection doit reposer sur une surveillance comportementale rigoureuse :

1.  **Surveillance des exécutions distantes :** Surveiller les lancements de `schtasks.exe` avec des arguments suspects et les exécutions de commandes PowerShell distantes.
2.  **Contrôle des accès sensibles :** Détecter l'accès aux processus critiques comme `lsass.exe` et surveiller les requêtes LDAP anormales utilisées pour la cartographie du réseau.
3.  **Analyse comportementale :**
    *   Repérer les patterns de communication C2 via des solutions NDR (Network Detection and Response).
    *   Utiliser les logs SIEM pour corréler les événements : lancements de processus suspects depuis des applications web, exécution de scripts encodés en Base64, et tentatives de dump de registres ou de fichiers de configuration.
4.  **Gestion des accès :** Appliquer le principe du moindre privilège, particulièrement sur les comptes de service et les comptes de domaine, afin de limiter l'efficacité des attaques type "Golden Ticket" ou DCSync.
5.  **Audit des outils système :** Surveiller l'usage détourné de LOLBINs (Living-off-the-land Binaries) comme `certutil.exe`, `reg.exe` et `powershell.exe`.

---
[Source](https://securelist.com/tr/cyberstrikeai-attacks/121715/){:target="_blank"}
