---
title: 'npm’s Update to Harden Their Supply Chain, and Points to Consider'
date: 2026-02-13
permalink: /posts/2026/02/13/npms-update-to-harden-their-supply-chain-and-points-to-consider/
tags:
- veille-cyber
- hackernews
---
### Renforcement de la Sécurité de la Chaîne d'Approvisionnement npm

npm a procédé à une refonte de son système d'authentification pour atténuer les attaques sur la chaîne d'approvisionnement, notamment suite à l'incident Shai-Hulud. Auparavant, npm utilisait des tokens "classiques" de longue durée, offrant un accès étendu qui, s'ils étaient compromis, permettaient aux attaquants de publier directement des versions malveillantes de paquets.

**Points Clés et Vulnérabilités:**

*   **Problème Initial:** Tokens "classiques" persistants et à large portée, facilitant la publication de code malveillant sans vérification de la source. Des incidents comme Shai-Hulud, Sha1-Hulud et chalk/debug illustrent ce risque.
*   **Solution npm:** Révocation de tous les tokens classiques et adoption par défaut de tokens basés sur des sessions. Les workflows interactifs utilisent désormais des tokens de session de courte durée (environ 2 heures) obtenus via `npm login`, avec l'authentification multifacteur (MFA) activée par défaut pour la publication. Encouragement de la publication de confiance via OIDC (OpenID Connect) pour obtenir des identifiants de courte durée par exécution.
*   **Vulnérabilités Persistantes:**
    *   **Phishing MFA:** Des tentatives de phishing ciblées sur la console npm, persuadant les mainteneurs de partager leurs identifiants de connexion et mots de passe à usage unique, peuvent toujours permettre l'obtention de tokens de courte durée suffisants pour introduire des logiciels malveillants.
    *   **MFA Optionnel sur Publication:** La MFA pour la publication reste facultative. Les développeurs peuvent créer des tokens de 90 jours avec contournement MFA activé, simulant ainsi les anciennes vulnérabilités des tokens classiques. L'accès à la console avec ces paramètres permet la publication de nouvelles versions malveillantes au nom de l'auteur.

**Recommandations:**

*   Promouvoir l'adoption généralisée d'OIDC à long terme pour une sécurité accrue.
*   Rendre la MFA obligatoire pour les chargements locaux de paquets (par code email ou OTP) et interdire les tokens personnalisés qui contournent la MFA.
*   Ajouter des métadonnées aux versions de paquets pour permettre aux développeurs d'identifier et d'éviter les paquets ou mainteneurs négligeant la sécurité de la chaîne d'approvisionnement.
*   Une approche consistant à construire les paquets à partir du code source vérifiable plutôt qu'à télécharger un artefact depuis npm (comme proposé par Chainguard Libraries) réduirait considérablement la surface d'attaque.

Bien que les récentes améliorations d'npm soient un pas positif, l'absence de MFA obligatoire pour toutes les publications et la persistance des risques liés au phishing signifient que le risque de compromission de la chaîne d'approvisionnement subsiste. L'adoption de multiples couches de sécurité, y compris la construction à partir de la source, est conseillée.

---
[Source](https://thehackernews.com/2026/02/npms-update-to-harden-their-supply.html){:target="_blank"}
