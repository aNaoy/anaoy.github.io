---
title: 'One-Click Microsoft 365 Copilot Flaw Could Have Let Attackers Steal Emails, Files, and MFA Codes'
date: 2026-06-15
permalink: /posts/2026/06/15/one-click-microsoft-365-copilot-flaw-could-have-let-attackers-steal-emails-files-and-mfa-codes/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité SearchLeak dans Microsoft 365 Copilot

Une faille critique, baptisée **SearchLeak**, permettait à un attaquant d'exfiltrer des données confidentielles (emails, fichiers OneDrive/SharePoint, codes MFA) via un simple clic sur un lien Microsoft légitime. L'attaque exploite une combinaison de trois vulnérabilités techniques pour contourner les protections de sécurité.

#### Points clés
*   **Mécanisme d'attaque :** L'attaquant utilise une injection de type "Prompt-to-Parameter" dans l'URL de recherche de Copilot. Le système interprète les paramètres comme des instructions plutôt que comme une simple requête.
*   **Exfiltration :** En exploitant une condition de concurrence (race condition) lors du rendu de la réponse, l'attaquant insère une balise `<img>` malveillante avant que le moteur de nettoyage ne puisse la bloquer.
*   **Contournement CSP :** L'attaque utilise les infrastructures de Bing comme proxy d'exfiltration. Comme Bing est autorisé par la politique de sécurité du contenu (CSP) de Microsoft, la requête de vol de données passe inaperçue auprès des outils de filtrage traditionnels.
*   **Impact :** Accès non autorisé à tout le contenu indexé par Microsoft Graph (données privées, identifiants temporaires, codes de double authentification).

#### Vulnérabilité identifiée
*   **CVE-2026-42824 :** Faille critique de type injection de commande permettant l'exfiltration d'informations. (Score CVSS : 6.5 à 7.5).

#### Recommandations
*   **Correctif :** Microsoft a déjà déployé une atténuation côté serveur ; aucune action directe n'est requise sur les instances des clients.
*   **Surveillance :** Les administrateurs doivent surveiller les logs à la recherche d'URL de recherche Copilot contenant des payloads encodés, du code HTML suspect, ou des requêtes inhabituelles vers les endpoints d'images de Bing.
*   **Gouvernance des données :** Réduire la surface d'exposition en restreignant les accès et l'indexation par Copilot aux seules données strictement nécessaires, limitant ainsi l'impact potentiel d'une future fuite de données.

---
[Source](https://thehackernews.com/2026/06/one-click-microsoft-365-copilot-flaw.html){:target="_blank"}
