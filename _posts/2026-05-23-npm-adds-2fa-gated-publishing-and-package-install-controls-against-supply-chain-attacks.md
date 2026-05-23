---
title: 'npm Adds 2FA-Gated Publishing and Package Install Controls Against Supply Chain Attacks'
date: 2026-05-23
permalink: /posts/2026/05/23/npm-adds-2fa-gated-publishing-and-package-install-controls-against-supply-chain-attacks/
tags:
- veille-cyber
- hackernews
---
### Sécurisation de la supply chain npm : Publication différée et nouveaux contrôles d'installation

GitHub a renforcé la sécurité de l'écosystème npm face à la recrudescence des attaques de la chaîne d'approvisionnement logicielle, notamment celles orchestrées par des groupes comme TeamPCP. Ces mesures visent à prévenir la compromission de packages en imposant une validation humaine et un contrôle strict des sources d'installation.

**Points clés :**
*   **Staged Publishing (Publication différée) :** Les packages ne sont plus publiés instantanément. Ils sont placés dans une file d'attente après leur téléchargement, nécessitant une approbation explicite via une authentification à deux facteurs (2FA) de la part d'un mainteneur avant de devenir publics.
*   **Contrôle des sources d'installation :** Introduction de nouveaux drapeaux (`flags`) pour restreindre les sources d'installation non-registre, limitant ainsi les vecteurs d'attaque par exécution de code arbitraire via des chemins locaux ou des URL distantes.
*   **Contexte de menace :** Cette mise à jour répond à une multiplication des empoisonnements de packages open-source à grande échelle.

**Vulnérabilités :**
*   Bien qu'aucune CVE spécifique ne soit mentionnée, ces mécanismes ciblent intrinsèquement la menace du **détournement de compte (Account Takeover)** et de l'**injection de code malveillant dans les pipelines CI/CD**, où un attaquant peut pousser des versions corrompues sans interaction humaine.

**Recommandations :**
*   **Activer le Staged Publishing :** Utiliser la commande `npm stage publish` (nécessite npm CLI 11.15.0 ou supérieur).
*   **Activer la 2FA :** Rendre obligatoire l'authentification à deux facteurs pour tous les comptes ayant des droits de publication.
*   **Combiner les stratégies :** Associer la publication différée avec la méthode de « Trusted Publishing » utilisant OIDC (OpenID Connect) pour renforcer la sécurité des flux de déploiement automatisés.
*   **Restreindre les installations :** Utiliser les nouveaux drapeaux (`--allow-file`, `--allow-remote`, `--allow-directory`) pour adopter une politique de liste blanche lors de l'installation de dépendances hors registre.

---
[Source](https://thehackernews.com/2026/05/npm-adds-2fa-gated-publishing-and.html){:target="_blank"}
