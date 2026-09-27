---
title: 'ShinyHunters uses WAF bypass trick in Oracle PeopleSoft attacks'
date: 2026-09-27
permalink: /posts/2026/09/27/shinyhunters-uses-waf-bypass-trick-in-oracle-peoplesoft-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Contournement de WAF par ShinyHunters : Menace persistante sur Oracle PeopleSoft

Le groupe de cybercriminels ShinyHunters (UNC6240) exploite une nouvelle technique pour contourner les règles de filtrage (WAF) protégeant les serveurs Oracle PeopleSoft. Alors que de nombreuses organisations utilisaient le blocage du chemin `/PSEMHUB/` comme mesure d'atténuation temporaire, les attaquants utilisent désormais l'encodage d'URL pour dissimuler leurs requêtes malveillantes.

**Points clés :**
* **Technique de contournement :** Les attaquants remplacent des caractères du chemin cible par leur équivalent encodé (ex: `/%50SEMHUB/` au lieu de `/PSEMHUB/`). Le WAF ne reconnaît pas le chemin bloqué, mais le serveur WebLogic décode la requête et exécute le code malveillant.
* **Impact :** Une nouvelle vague d'attaques a été observée mondialement, touchant divers secteurs (éducation, santé, gouvernement).
* **Mode opératoire :**
    * Analyse préliminaire par envoi de requêtes sérialisées pour vérifier la vulnérabilité.
    * Déploiement de *web shells* (`x.jsp`, `u.jsp`, `tunnel.jsp`) pour exécuter des commandes.
    * Installation de malwares (backdoor SIDEEYE, outil Neo-reGeorg) pour le vol de données et le mouvement latéral dans les réseaux internes.

**Vulnérabilité exploitée :**
* **CVE-2026-35273 :** Exécution de code à distance (RCE) non authentifiée dans le composant PSEMHUB d'Oracle PeopleSoft.

**Recommandations :**
* **Priorité absolue :** Appliquer les correctifs de sécurité officiels fournis par Oracle plutôt que de se reposer sur des règles WAF, qui sont désormais facilement contournables.
* **Détection :** Analyser les logs d'accès WebLogic à la recherche de requêtes ciblant `/PSEMHUB/` et toutes ses variantes encodées (ex: `/%50SEMHUB/`).
* **Audit :** Rechercher la présence de fichiers suspects (`x.jsp`, `u.jsp`, `u2.jsp`, `tunnel.jspx`, `Ple64.exe`) ou de comportements anormaux liés à des processus de gestion à distance comme MeshAgent.

---
[Source](https://www.bleepingcomputer.com/news/security/shinyhunters-uses-waf-bypass-trick-in-oracle-peoplesoft-attacks/){:target="_blank"}
