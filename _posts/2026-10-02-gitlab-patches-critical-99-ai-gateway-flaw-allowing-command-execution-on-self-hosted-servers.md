---
title: 'GitLab Patches Critical 9.9 AI Gateway Flaw Allowing Command Execution on Self-Hosted Servers'
date: 2026-10-02
permalink: /posts/2026/10/02/gitlab-patches-critical-99-ai-gateway-flaw-allowing-command-execution-on-self-hosted-servers/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique d'exécution de code dans GitLab AI Gateway

Une vulnérabilité critique affecte le service **AI Gateway** de GitLab, permettant à un utilisateur authentifié disposant d'un accès à la plateforme "Duo Agent" d'exécuter des commandes arbitraires sur le serveur. Cette faille ne concerne que les organisations ayant déployé leur propre passerelle AI (self-hosted).

**Points clés :**
*   **Risque :** Exécution de code à distance (RCE).
*   **Portée :** Concerne exclusivement les déploiements auto-hébergés. Les instances GitLab.com, GitLab Dedicated et celles utilisant la passerelle gérée par GitLab ne sont pas vulnérables.
*   **État de l'exploitation :** Aucune preuve d'exploitation active n'a été signalée à ce jour.
*   **Origine :** Le problème réside dans une faiblesse du moteur de template lors de la configuration de flux personnalisés (CWE-1336).

**Vulnérabilité identifiée :**
*   **CVE-2026-90970** : Score CVSS de **9.9/10**.

**Versions corrigées :**
Il est impératif de mettre à jour les images Docker ou les chartes Helm vers les versions suivantes :
*   Pour la branche 19.4 : **19.4.1**
*   Pour la branche 19.3 : **19.3.2**
*   Pour la branche 19.2 : **19.2.4**

**Recommandations :**
*   **Mise à jour immédiate :** Les administrateurs doivent arrêter, supprimer et redéployer leurs conteneurs AI Gateway avec les tags de version corrigés.
*   **Vérification :** Aucune mesure de contournement n'a été publiée ; la mise à jour logicielle est la seule protection contre cette vulnérabilité.
*   **Gestion des accès :** Bien que la faille nécessite un accès utilisateur, il est conseillé de limiter strictement les permissions sur la plateforme "Duo Agent" par mesure de sécurité renforcée.

---
[Source](https://thehackernews.com/2026/10/gitlab-patches-critical-self-hosted-ai.html){:target="_blank"}
