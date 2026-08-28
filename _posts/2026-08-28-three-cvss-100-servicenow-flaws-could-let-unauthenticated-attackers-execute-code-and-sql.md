---
title: 'Three CVSS 10.0 ServiceNow Flaws Could Let Unauthenticated Attackers Execute Code and SQL'
date: 2026-08-28
permalink: /posts/2026/08/28/three-cvss-100-servicenow-flaws-could-let-unauthenticated-attackers-execute-code-and-sql/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans la plateforme ServiceNow

ServiceNow a publié des correctifs pour quatre vulnérabilités affectant sa plateforme AI, dont trois sont classées avec un score de criticité maximale (CVSS 10.0). Ces failles permettent, dans certaines conditions, à un attaquant non authentifié d'exécuter du code arbitraire, de modifier des données ou d'effectuer des injections SQL.

**Points clés :**
*   Les trois vulnérabilités CVSS 10.0 présentent une complexité d'attaque faible, ne nécessitant ni privilèges ni interaction utilisateur.
*   ServiceNow a automatiquement mis à jour ses instances hébergées.
*   Les organisations utilisant des instances auto-hébergées doivent appliquer les correctifs manuellement de toute urgence.
*   Aucune exploitation active de ces quatre nouvelles vulnérabilités n'a été confirmée à ce jour.

**Vulnérabilités identifiées :**
*   **CVE-2026-18885 (CVSS 10.0) :** Injection de code dans l'API GraphQL Composite Data, permettant l'exécution de code arbitraire et l'accès aux données de l'instance.
*   **CVE-2026-18886 (CVSS 10.0) :** Contrôle d'accès défaillant dans le processeur de téléchargement d'images, pouvant mener à une élévation de privilèges.
*   **CVE-2026-74820 (CVSS 10.0) :** Injection SQL via la clause `ORDER BY` du schéma dynamique.
*   **CVE-2026-6876 (CVSS 8.7) :** Évasion de bac à sable (*sandbox*) dans la plateforme Now, permettant l'exécution de code.

**Recommandations :**
*   **Mise à jour immédiate :** Les administrateurs doivent vérifier la version de leur instance (versions Xanadu, Yokohama, Zurich et Australia) et appliquer les correctifs spécifiques mentionnés dans l'avis de sécurité officiel.
*   **Vérification des instances :** Consulter la [base de connaissances ServiceNow (KB3152242)](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3152242) pour identifier si votre version est vulnérable et obtenir les patchs correctifs correspondants.

---
[Source](https://thehackernews.com/2026/08/three-cvss-100-servicenow-flaws-could.html){:target="_blank"}
