---
title: 'GitHub Tightens npm Publishing After Flaw Left 1,500+ Packages Vulnerable to Hijacking'
date: 2026-10-13
permalink: /posts/2026/10/13/github-tightens-npm-publishing-after-flaw-left-1500-packages-vulnerable-to-hijacking/
tags:
- veille-cyber
- hackernews
---
### Sécurisation du mécanisme "Trusted Publishing" sur npm suite à la faille SlugFest

GitHub a renforcé la sécurité du processus de publication des paquets npm afin de contrer une vulnérabilité critique, surnommée **SlugFest**, qui permettait à des attaquants de détourner des paquets sans voler d'identifiants.

**Points clés :**
*   **La faille :** Le système de *Trusted Publishing* (basé sur OIDC) reposait sur le nom ("slug") du dépôt GitHub (ex: `propriétaire/dépôt`) plutôt que sur son identifiant unique immuable. Lorsqu'un mainteneur renommait ou transférait un dépôt, l'ancien nom devenait disponible. Un attaquant pouvait alors réclamer ce nom, créer un nouveau dépôt et hériter des droits de publication sur le paquet npm associé, à condition qu'aucune publication n'ait encore eu lieu via cette configuration.
*   **Impact :** Plus de 1 500 paquets (cumulant 10 millions de téléchargements) étaient vulnérables à des attaques de type "supply chain". Un attaquant pouvait injecter du code malveillant dans des versions légitimes, lequel était automatiquement propagé par les outils de développement et les agents IA.
*   **Correction :** GitHub impose désormais une fenêtre de validation de 48 heures pour les nouvelles configurations de confiance. Passé ce délai, si aucune publication n'a été effectuée, la configuration expire. Une première publication réussie lie définitivement la configuration à l'identifiant immuable du dépôt GitHub.

**Vulnérabilités :**
*   **CVE :** Aucune CVE n'a été attribuée à ce jour pour cette faille logique, bien que l'impact soit majeur pour la chaîne d'approvisionnement logicielle.

**Recommandations pour les développeurs :**
*   **Auditer les configurations :** Vérifier que les "slugs" des dépôts liés dans les paramètres de confiance correspondent toujours aux dépôts actifs.
*   **Mise à jour post-migration :** Si un dépôt est renommé, transféré ou supprimé, il est impératif de supprimer manuellement l'ancienne configuration de confiance et d'en créer une nouvelle.
*   **Surveillance :** Surveiller étroitement les événements de publication npm pour détecter toute activité inhabituelle.
*   **Hygiène des dépôts :** Supprimer systématiquement les liaisons de confiance lors de la suppression ou du changement de nom d'un dépôt GitHub.

---
[Source](https://thehackernews.com/2026/10/github-tightens-npm-publishing-after.html){:target="_blank"}
