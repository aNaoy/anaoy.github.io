---
title: 'Ivanti: Max severity Sentry flaw allows code execution as root'
date: 2026-06-10
permalink: /posts/2026/06/10/ivanti-max-severity-sentry-flaw-allows-code-execution-as-root/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilités critiques dans la solution Ivanti Sentry

Ivanti a corrigé deux vulnérabilités critiques affectant sa passerelle de sécurité mobile Sentry (anciennement MobileIron Sentry). Bien qu'aucune preuve d'exploitation active n'ait été détectée à ce jour, la sévérité des failles impose une vigilance immédiate.

**Points clés :**
*   Les vulnérabilités permettent à des attaquants distants de compromettre totalement l'intégrité du système.
*   Ivanti Sentry est un équipement critique sécurisant les flux entre les systèmes d'entreprise et les terminaux mobiles.
*   Aucune exploitation "in the wild" n'est connue à ce jour, mais les produits Ivanti sont fréquemment ciblés par des groupes cybercriminels.

**Vulnérabilités identifiées :**
*   **CVE-2026-10520 :** Injection de commande OS permettant une exécution de code à distance avec les privilèges root (gravité maximale).
*   **CVE-2026-10523 :** Contournement d'authentification permettant à un attaquant non authentifié de créer des comptes administrateurs et d'obtenir un accès complet au système.

**Recommandations :**
*   Appliquer immédiatement les correctifs fournis par Ivanti en mettant à jour les instances vers les versions **R10.5.2, R10.6.2 ou R10.7.1**.
*   Surveiller les journaux système pour détecter toute création de compte administrateur suspecte ou activité inhabituelle sur les appliances Sentry.

---
[Source](https://www.bleepingcomputer.com/news/security/new-max-severity-ivanti-sentry-flaw-allows-code-execution-as-root/){:target="_blank"}
