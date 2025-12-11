---
title: 'New ConsentFix attack hijacks Microsoft accounts via Azure CLI'
date: 2025-12-11
permalink: /posts/2025/12/11/new-consentfix-attack-hijacks-microsoft-accounts-via-azure-cli/
tags:
- veille-cyber
- bleepingcomp
---
### Dérobe de Compte Microsoft via Azure CLI

Une nouvelle technique d'ingénierie sociale, nommée "ConsentFix", exploite la ligne de commande Azure (Azure CLI) pour s'emparer de comptes Microsoft. Elle contourne le besoin de mot de passe et d'authentification multifacteur (MFA).

Le processus débute par l'attraction de victimes vers un site compromis, où un faux CAPTCHA Cloudflare Turnstile demande une adresse e-mail professionnelle. Après validation, l'utilisateur est incité à cliquer sur un bouton "Se connecter". Celui-ci ouvre une authentification Azure, générant un code d'autorisation OAuth pour l'Azure CLI. Si l'utilisateur est déjà connecté à son compte Microsoft, aucune nouvelle authentification n'est nécessaire.

La victime est ensuite invitée à coller l'URL de redirection, contenant le code volé, sur la page frauduleuse. Ce code permet aux attaquants d'obtenir un jeton d'accès Azure CLI, leur conférant un contrôle total sur le compte Microsoft compromis.

**Points Clés :**

*   **Exploitation de l'Azure CLI :** La vulnérabilité repose sur le flux d'authentification OAuth de l'Azure CLI.
*   **Contournement de la sécurité :** Le mot de passe et la MFA sont évités grâce au vol du code d'autorisation.
*   **Ingénierie sociale :** Utilisation de faux CAPTCHAs et d'instructions trompeuses pour pousser la victime à coopérer.
*   **Filtrage des cibles :** La demande d'e-mail professionnel permet de cibler spécifiquement les individus souhaités.
*   **Automatisation :** Une fois les étapes suivies, l'accès est immédiat pour l'attaquant.

**Vulnérabilités :**

*   Bien qu'aucun numéro CVE spécifique ne soit mentionné dans l'article, l'attaque exploite la manière dont l'Azure CLI gère les flux OAuth et les autorisations. La vulnérabilité réside dans la capacité à extraire et utiliser un code d'autorisation sans authentification supplémentaire.

**Recommandations :**

*   **Surveillance des connexions Azure :** Rechercher des activités de connexion inhabituelles via l'Azure CLI, telles que des connexions provenant de nouvelles adresses IP.
*   **Suivi des scopes d'autorisation :** Surveiller l'utilisation de scopes (permissions) hérités ou suspects dans les autorisations accordées à l'Azure CLI, car ils peuvent être utilisés pour contourner les détections.
*   **Sensibilisation des utilisateurs :** Éduquer les utilisateurs sur les techniques d'ingénierie sociale, en particulier celles qui les incitent à interagir avec des flux d'authentification ou à copier-coller des informations sensibles.

---
[Source](https://www.bleepingcomputer.com/news/security/new-consentfix-attack-hijacks-microsoft-accounts-via-azure-cli/){:target="_blank"}
