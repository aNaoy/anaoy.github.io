---
title: 'New Phoenix attack bypasses Rowhammer defenses in DDR5 memory'
date: 2025-09-15
permalink: /posts/2025/09/15/new-phoenix-attack-bypasses-rowhammer-defenses-in-ddr5-memory/
tags:
- veille-cyber
- bleepingcomp
---
### Phoenix : Une nouvelle attaque Rowhammer contourne les protections DDR5

Une nouvelle variante d'attaque Rowhammer, nommée Phoenix, a été développée par des chercheurs de l'ETH Zurich et de Google. Cette attaque exploite les nouvelles générations de mémoire DDR5 en contournant les mécanismes de défense, notamment le Targeted Row Refresh (TRR). Les attaques Rowhammer classiques fonctionnent en accédant rapidement et de manière répétée à des lignes de mémoire spécifiques, provoquant des interférences électriques qui peuvent altérer les données (bit flips).

Les chercheurs ont découvert des failles dans les implémentations de TRR de SK Hynix, permettant à Phoenix de synchroniser et d'exploiter des intervalles de rafraîchissement manqués. L'attaque a réussi à inverser des bits sur tous les modules DDR5 testés et a permis une escalade de privilèges en moins de deux minutes sur un système standard. Des tests ont également démontré la possibilité de lire/écrire arbitrairement en mémoire, de compromettre des clés SSH, et d'altérer des binaires pour obtenir un accès root.

**Points Clés :**

*   **Attaque Phoenix :** Nouvelle variante de Rowhammer ciblant la mémoire DDR5.
*   **Contournement des défenses :** Efficace contre les mécanismes de protection TRR.
*   **Exploitation de failles :** Exploite des intervalles de rafraîchissement spécifiques et manqués.
*   **Impact :** Possibilité d'escalade de privilèges, corruption de données, accès à des informations sensibles, et prise de contrôle du système.

**Vulnérabilités :**

*   **CVE-2025-6202 :** Nom attribué à l'attaque Phoenix.
*   **Affecte :** Tous les modules RAM DIMM produits entre janvier 2021 et décembre 2024.
*   **Tests :**
    *   100% des modules DDR5 testés vulnérables à au moins un schéma d'attaque.
    *   Exploitation des entrées de table de pages (PTE) pour lecture/écriture arbitraire.
    *   73% des modules exposés à la compromission de clés SSH (RSA-2048).
    *   33% des modules permettent l'altération du binaire `sudo` pour une escalade de privilèges locale.

**Recommandations :**

*   **Modification des intervalles de rafraîchissement :** Tripler l'intervalle de rafraîchissement de la DRAM (tREFI) est proposé comme solution pour stopper les attaques Phoenix.
*   **Considération des risques :** Cette modification peut potentiellement causer des erreurs ou de la corruption de données, rendant le système instable.

---
[Source](https://www.bleepingcomputer.com/news/security/new-phoenix-attack-bypasses-rowhammer-defenses-in-ddr5-memory/){:target="_blank"}
