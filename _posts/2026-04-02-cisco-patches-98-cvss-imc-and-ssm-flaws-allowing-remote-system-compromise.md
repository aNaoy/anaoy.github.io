---
title: 'Cisco Patches 9.8 CVSS IMC and SSM Flaws Allowing Remote System Compromise'
date: 2026-04-02
permalink: /posts/2026/04/02/cisco-patches-98-cvss-imc-and-ssm-flaws-allowing-remote-system-compromise/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques chez Cisco : Risques d'accès total et exécution de commandes

Cisco a publié des correctifs pour deux vulnérabilités critiques (score CVSS de 9,8/10) affectant ses équipements réseau et ses solutions de gestion. Ces failles permettent à un attaquant distant non authentifié de compromettre totalement les systèmes visés.

**Points clés :**
*   **CVE-2026-20093 (IMC) :** Une mauvaise gestion des demandes de changement de mot de passe permet de contourner l'authentification. Un attaquant peut modifier le mot de passe de n'importe quel utilisateur, y compris celui de l'administrateur, pour prendre le contrôle du système.
*   **CVE-2026-20160 (SSM On-Prem) :** Une exposition non intentionnelle d'un service interne permet à un attaquant d'envoyer une requête API contrefaite pour exécuter des commandes arbitraires avec des privilèges root sur le système d'exploitation sous-jacent.
*   **État de la menace :** Aucune exploitation active n'a été signalée pour le moment, mais la criticité des failles impose une vigilance immédiate.

**Recommandations :**
*   **Mise à jour immédiate :** Appliquer les correctifs fournis par Cisco sans attendre.
*   **Versions corrigées :**
    *   **IMC :** Mettre à jour vers les versions spécifiées (ex: 4.15.5 pour ENCS 5000, 4.18.3 pour Catalyst 8300, et versions correspondantes pour les serveurs UCS C-Series et E-Series).
    *   **SSM On-Prem :** Mettre à jour vers la version **9-202601**.
*   **Contournement :** Aucune solution de contournement n'étant disponible, la mise à jour logicielle est la seule mesure de protection efficace.

---
[Source](https://thehackernews.com/2026/04/cisco-patches-98-cvss-imc-and-ssm-flaws.html){:target="_blank"}
