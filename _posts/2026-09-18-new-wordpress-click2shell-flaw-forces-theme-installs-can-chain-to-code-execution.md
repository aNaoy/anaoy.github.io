---
title: 'New WordPress Click2Shell Flaw Forces Theme Installs, Can Chain to Code Execution'
date: 2026-09-18
permalink: /posts/2026/09/18/new-wordpress-click2shell-flaw-forces-theme-installs-can-chain-to-code-execution/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité "Click2Shell" dans WordPress : Risque d'exécution de code à distance

Une nouvelle vulnérabilité, baptisée **Click2Shell**, a été découverte dans le cœur de WordPress. Elle permet à un attaquant de forcer l'installation d'un thème depuis le répertoire officiel sans l'intervention de l'administrateur. Si elle est combinée à une faille présente dans un thème spécifique, cette attaque peut mener à une exécution de code arbitraire sur le serveur.

**Points clés :**
*   **Mécanisme :** L'attaque repose sur un lien piégé cliqué par un administrateur connecté. Le navigateur de l'administrateur interprète mal les paramètres de l'URL, ce qui déclenche automatiquement le bouton d'installation du thème.
*   **Chaînage :** L'installation forcée d'un thème vulnérable (contenant des failles de traitement de données sans vérification d'autorisation) permet ensuite à l'attaquant d'exécuter son propre code malveillant sur le serveur.
*   **État de la menace :** Aucune preuve d'exploitation active n'a été constatée à ce jour.

**Vulnérabilités :**
*   **CVE :** Aucune assignée pour le moment.
*   **Sévérité :** Score CVSS de 7.1 pour l'installation forcée isolée, et jusqu'à 9.6 pour la chaîne complète menant à l'exécution de code.
*   **Versions affectées :** De la version 6.0 jusqu'aux versions précédant la 7.1.1.

**Recommandations :**
*   **Mise à jour immédiate :** Appliquer le correctif de sécurité via la version **WordPress 7.1.1** (ou les mises à jour de maintenance correspondantes pour les anciennes branches).
*   **Bonnes pratiques :** Puisque l'attaque nécessite qu'un administrateur clique sur un lien malveillant, la vigilance face aux liens suspects reste une mesure de protection indispensable. Les sites configurés pour les mises à jour automatiques devraient recevoir le correctif sans action supplémentaire.

---
[Source](https://thehackernews.com/2026/09/new-wordpress-click2shell-flaw-forces.html){:target="_blank"}
