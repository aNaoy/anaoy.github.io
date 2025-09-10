---
title: 'Microsoft Patch Tuesday, September 2025 Edition'
date: 2025-09-10
permalink: /posts/2025/09/10/microsoft-patch-tuesday-september-2025-edition/
tags:
- veille-cyber
- krebs
---
### Patchs de Sécurité Microsoft : Septembre 2025

Microsoft a publié des mises à jour corrigeant plus de 80 vulnérabilités affectant ses systèmes d'exploitation et logiciels. Aucune vulnérabilité critique exploitée activement (zero-day) n'est signalée pour ce lot, mais 13 failles classées comme "critiques" sont corrigées. D'autres acteurs comme Apple et Google ont récemment mis à jour leurs systèmes pour remédier à des bugs zero-day.

**Points Clés :**

*   Plus de 80 vulnérabilités corrigées par Microsoft.
*   13 vulnérabilités critiques sont incluses dans ces mises à jour.
*   Aucune exploitation zero-day activement constatée dans les patchs Microsoft de ce mois-ci.
*   D'autres mises à jour récentes d'Apple et Google ont corrigé des failles zero-day.

**Vulnérabilités Notables :**

*   **CVE-2025-54918** : Affecte Windows NTLM. Bien que classée comme une élévation de privilèges, elle est considérée comme exploitable à distance via le réseau. Elle permettrait à un attaquant d'obtenir des privilèges SYSTEME sur la machine cible en envoyant des paquets spécialement conçus. Elle nécessite potentiellement que l'attaquant possède déjà le hachage NTLM ou les identifiants de l'utilisateur.
*   **CVE-2025-55234** : Affecte le client Windows SMB. Également une élévation de privilèges, cette faille est également exploitable à distance. Elle permet une attaque par rejeu (replay attack) pouvant mener à l'exécution de code. Cette vulnérabilité avait été divulguée publiquement avant ces mises à jour.
*   **CVE-2025-54916** : Affecte Windows NTFS. Classée comme "importante", elle permet l'exécution de code à distance. L'exploitation n'est pas directement possible sur le réseau mais nécessite que l'attaquant puisse exécuter du code sur l'hôte ou de tromper un utilisateur pour qu'il exécute un fichier malveillant (par exemple, via des attaques d'ingénierie sociale). Microsoft anticipe une exploitation probable, rappelant qu'une faille NTFS précédente avait été exploitée en zero-day.

Parmi les corrections de ce mois-ci, près de la moitié concernent des vulnérabilités d'élévation de privilèges, nécessitant un accès préalable au système cible.

**Recommandations :**

*   Appliquer les mises à jour de sécurité de Microsoft dès que possible.
*   Effectuer des sauvegardes régulières des données.
*   Faire preuve de vigilance face aux tentatives d'ingénierie sociale qui pourraient mener à l'exécution de fichiers malveillants.

---
[Source](https://krebsonsecurity.com/2025/09/microsoft-patch-tuesday-september-2025-edition/){:target="_blank"}
