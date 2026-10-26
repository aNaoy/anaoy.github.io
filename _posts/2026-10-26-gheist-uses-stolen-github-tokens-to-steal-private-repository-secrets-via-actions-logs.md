---
title: 'Gheist Uses Stolen GitHub Tokens to Steal Private Repository Secrets via Actions Logs'
date: 2026-10-26
permalink: /posts/2026/10/26/gheist-uses-stolen-github-tokens-to-steal-private-repository-secrets-via-actions-logs/
tags:
- veille-cyber
- hackernews
---
### Campagne « Gheist » : Vol massif de secrets via les GitHub Actions

La campagne « Gheist » exploite des jetons d'accès GitHub volés pour automatiser l'exfiltration de secrets de dépôts privés et d'environnements GitHub Enterprise. Les attaquants injectent des workflows malveillants, téléchargent les journaux d'exécution (logs) contenant les secrets encodés en base32, puis suppriment les traces de leurs actions.

#### Points clés
*   **Mode opératoire :** Utilisation de jetons compromis pour créer des branches nommées `ci-sync-[6 caractères aléatoires]` et pusher un fichier de workflow (`.github/workflows/sync-check.yml`).
*   **Méthode d'exfiltration :** Le workflow imprime les secrets de l'environnement, les encodent en base32 pour contourner le masquage automatique de GitHub, puis les envoie vers les attaquants.
*   **Ciblage :** La technique contourne les protections de GitHub sur les dépôts publics (qui bloquent les workflows suspects), mais reste très efficace sur les dépôts privés et les serveurs GitHub Enterprise.
*   **Expansion :** Des variantes visent désormais les *self-hosted runners* pour tenter de voler des identifiants locaux et des rôles cloud (AWS, Kubernetes).

#### Vulnérabilités
*   **Absence de filtrage automatique :** Les protections de sécurité de GitHub (workflow approval) ne s'appliquent pas par défaut aux dépôts privés ou à GitHub Enterprise.
*   **Droits d'accès :** Tout utilisateur disposant d'un droit d'écriture peut lire l'ensemble des secrets configurés dans un dépôt.

#### Recommandations
*   **Audit immédiat :** Rechercher des branches `ci-sync-*`, des commits avec le message « ci: sync config » et des activités suspectes associées au user-agent `gheist`.
*   **Remédiation post-compromission :**
    *   Révoquer immédiatement les jetons ayant poussé les commits malveillants.
    *   Effectuer une rotation complète de tous les secrets du dépôt et des environnements associés.
    *   Considérer comme compromis tout *self-hosted runner* ayant exécuté un de ces workflows.
*   **Durcissement de la sécurité :**
    *   Remplacer les jetons d'accès personnels (PAT) par des GitHub Apps ou des jetons affinés (fine-grained) à durée de vie limitée.
    *   Restreindre les politiques de confiance OIDC aux branches ou environnements protégés.
    *   Exiger l'approbation de réviseurs pour l'accès aux environnements contenant des secrets de production.
    *   Isoler les *self-hosted runners* en utilisant des machines éphémères sans accès direct aux métadonnées cloud.

---
[Source](https://thehackernews.com/2026/10/gheist-uses-stolen-github-tokens-to.html){:target="_blank"}
