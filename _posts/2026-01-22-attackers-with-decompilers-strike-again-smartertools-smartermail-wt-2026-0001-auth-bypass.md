---
title: 'Attackers With Decompilers Strike Again (SmarterTools SmarterMail WT-2026-0001 Auth Bypass)'
date: 2026-01-22
permalink: /posts/2026/01/22/attackers-with-decompilers-strike-again-smartertools-smartermail-wt-2026-0001-auth-bypass/
tags:
- veille-cyber
- zerodaysfans
---
## Contournement d'authentification et exécution de code à distance dans SmarterMail

Une vulnérabilité critique (WT-2026-0001) a été découverte dans SmarterTools SmarterMail permettant à n'importe quel utilisateur non authentifié de réinitialiser le mot de passe de l'administrateur système. Cette faille, rendue possible par une mauvaise gestion de l'endpoint `force-reset-password`, permettait l'envoi d'un JSON malveillant contenant le nom d'utilisateur de l'administrateur et le nouveau mot de passe souhaité, sans aucune vérification de l'ancien mot de passe ou autorisation.

Une fois l'accès administrateur obtenu, les attaquants peuvent exploiter une fonctionnalité intégrée de SmarterMail pour exécuter des commandes arbitraires au niveau du système d'exploitation, transformant ainsi la faille de contournement d'authentification en une capacité d'exécution de code à distance (RCE). Cette RCE est obtenue via la configuration des "Volume Mounts" dans les paramètres de l'application, où une commande spécifiée est exécutée par le système sous-jacent.

Cette vulnérabilité a été corrigée par SmarterTools dans la version 9511, publiée le 15 janvier 2026. Cependant, des rapports indiquent que cette faille est déjà activement exploitée, avec des tentatives de compromission observées peu après la publication du correctif. Les attaquants auraient réussi à reconstruire la vulnérabilité en analysant les notes de mise à jour, potentiellement en utilisant des décompilateurs.

### Points clés :

*   **Vulnérabilité :** WT-2026-0001 - Contournement d'authentification permettant la réinitialisation du mot de passe administrateur.
*   **Conséquence directe :** Obtention de l'accès administrateur système.
*   **Conséquence secondaire :** Exécution de code à distance (RCE) via la fonctionnalité de "Volume Mounts".
*   **Méthode d'exploitation :** Envoi d'une requête POST à l'endpoint `/api/v1/auth/force-reset-password` avec un corps JSON spécifiant `IsSysAdmin: "true"`, le nom d'utilisateur de l'administrateur et un nouveau mot de passe.
*   **Exploitation observée :** La vulnérabilité est activement exploitée peu de temps après la publication du correctif.
*   **Cause probable de la reconstruction de la vulnérabilité :** Analyse des notes de mise à jour et ingénierie inverse par les attaquants.

### Vulnérabilités identifiées :

*   **WT-2026-0001 :** Authentication Bypass via password reset.
    *   **CVE :** Non assigné au moment de la rédaction de l'article.

### Recommandations :

*   **Mettre à jour SmarterMail immédiatement** vers la version 9511 ou une version ultérieure pour corriger la vulnérabilité WT-2026-0001.
*   Être vigilant quant aux tentatives d'exploitation, notamment celles qui ciblent la fonctionnalité de réinitialisation de mot de passe.
*   Surveiller les journaux système pour détecter toute activité suspecte liée à la modification des mots de passe administrateur ou à l'exécution de commandes non autorisées.

---
[Source](https://labs.watchtowr.com/attackers-with-decompilers-strike-again-smartertools-smartermail-wt-2026-0001-auth-bypass/){:target="_blank"}
