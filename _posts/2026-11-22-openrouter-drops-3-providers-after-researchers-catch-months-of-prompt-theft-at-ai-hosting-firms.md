---
title: 'OpenRouter Drops 3 Providers After Researchers Catch Months of Prompt Theft at AI Hosting Firms'
date: 2026-11-22
permalink: /posts/2026/11/22/openrouter-drops-3-providers-after-researchers-catch-months-of-prompt-theft-at-ai-hosting-firms/
tags:
- veille-cyber
- hackernews
---
### Vol de données massif chez les fournisseurs d'IA : failles de confidentialité et détournement de prompts

Des chercheurs ont découvert que des attaquants infiltrent les infrastructures de fournisseurs d'IA depuis plusieurs mois pour intercepter les requêtes des utilisateurs, y compris celles marquées comme « Zero Data Retention » (absence de rétention de données). 

**Points clés :**
*   **Vol systématique :** Les attaquants capturent les prompts dès le point d'arrivée pour en extraire des identifiants (AWS, clés API, mots de passe).
*   **Inopérance des drapeaux de confidentialité :** Les promesses de non-rétention sont ignorées ou contournées dès qu'un attaquant accède à l'infrastructure interne.
*   **Vecteurs d'attaque :** Compromission de serveurs d'inférence, erreurs de routage, logging malveillant par des vendeurs peu scrupuleux, et fuites de données vers des laboratoires tiers (notamment en Chine).
*   **Preuve par « Canary Tokens » :** L'utilisation de jetons de suivi uniques a permis de confirmer que les données étaient lues par des humains et utilisées pour des accès non autorisés.
*   **Réaction d'OpenRouter :** La plateforme a retiré trois fournisseurs de son service et suspendu l'éligibilité au « Zero Data Retention » pour 125 points de terminaison suspects.

**Vulnérabilités :**
*   Absence de sécurisation des données aux points de terminaison intermédiaires (fournisseurs tiers).
*   Mauvaises configurations de routage réseau permettant l'interception du trafic.
*   Fuite d'informations sensibles (clés AWS, jetons) dans les prompts, exploitées via des outils comme *ARTEX*.
*   *Note : Aucune CVE spécifique n'est associée, les incidents étant liés à des compromissions opérationnelles et des erreurs de conception.*

**Recommandations :**
*   **Rotation des secrets :** Considérer comme compromis tout identifiant (clés API, mots de passe) ayant transité par un fournisseur d'inférence tiers.
*   **Sécurisation du routage :** Éviter les places de marché (resellers) opaques et privilégier la sélection directe des fournisseurs de premier rang.
*   **Auto-hébergement :** Privilégier l'auto-hébergement des modèles lorsque la confidentialité des données est critique.
*   **Systèmes d'alerte :** Intégrer des *canary tokens* dans les prompts pour détecter immédiatement toute lecture ou utilisation non autorisée.
*   **Hygiène des données :** Désinfecter les prompts avant envoi pour supprimer toute clé ou identifiant sensible, et mettre en place des outils de détection automatique des fuites de secrets.

---
[Source](https://thehackernews.com/2026/11/openrouter-drops-3-providers-after.html){:target="_blank"}
