---
title: 'Microsoft Copilot Personal Flaws Could Let One Click Exfiltrate Data From Connected Apps'
date: 2026-08-18
permalink: /posts/2026/08/18/microsoft-copilot-personal-flaws-could-let-one-click-exfiltrate-data-from-connected-apps/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans Microsoft Copilot Personal : La menace "CoSnitch"

Varonis Threat Labs a identifié un ensemble de vulnérabilités, baptisé **CoSnitch**, affectant Microsoft Copilot Personal. Ces failles permettent à un attaquant, via un lien piégé, d'exfiltrer silencieusement des données provenant d'applications connectées ou d'empoisonner la mémoire de l'assistant IA.

**Points clés :**
*   **Exécution automatique :** Une combinaison de paramètres d'URL (`autorun=1` et `q`) permet de forcer l'exécution d'invites (prompts) malveillantes dès le chargement de la page, sans interaction de la victime.
*   **Exfiltration de données :** Une fois activé, l'IA peut interroger des services autorisés (Google Drive, emails, calendrier) et envoyer les informations récoltées vers un serveur distant.
*   **Persistance de la mémoire :** Une faille distincte lors de la synthèse de pages web permet d'écrire des instructions malveillantes directement dans la mémoire de long terme de l'utilisateur. Ces instructions persistent même après un changement de mot de passe ou une reconnexion, jusqu'à une suppression manuelle.
*   **Discrétion :** L'exfiltration imite les comportements légitimes de Copilot et ne laisse aucune trace dans les journaux de sécurité classiques.

**Vulnérabilité identifiée :**
*   **CVE-2026-24301** : Concerne l'exécution automatique de prompts et l'exfiltration via les services connectés.

**Recommandations :**
*   **Audit des connexions :** Passer en revue les applications tierces liées à Copilot et révoquer les accès aux services qui ne sont plus nécessaires.
*   **Vigilance accrue :** Faire preuve d'une prudence extrême face aux liens pointant vers des assistants IA.
*   **Nettoyage de la mémoire :** Vérifier régulièrement les paramètres de mémoire de Copilot pour supprimer toute instruction ou règle non autorisée ou suspecte.
*   **Approche « Zero Trust » :** Considérer l'assistant IA comme un utilisateur privilégié nécessitant une surveillance constante des activités anormales.

---
[Source](https://thehackernews.com/2026/08/microsoft-copilot-personal-flaws-could.html){:target="_blank"}
