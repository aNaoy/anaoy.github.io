---
title: 'Ukraine identifies infostealer operator tied to 28,000 stolen accounts'
date: 2026-05-21
permalink: /posts/2026/05/21/ukraine-identifies-infostealer-operator-tied-to-28000-stolen-accounts/
tags:
- veille-cyber
- bleepingcomp
---
### Démantèlement d'un réseau de vol d'identifiants par "infostealer"

La police cybernétique ukrainienne, en collaboration avec les autorités américaines, a identifié un individu de 18 ans basé à Odessa, suspecté d'être l'opérateur principal d'une campagne de logiciels malveillants de type *infostealer*. Entre 2024 et 2025, cette opération a compromis 28 000 comptes clients d'une boutique en ligne californienne, permettant des achats frauduleux pour un montant de 721 000 $.

**Points clés :**
*   **Mode opératoire :** Le suspect utilisait des malwares pour dérober des jetons de session, des cookies de navigateur et des identifiants de connexion.
*   **Impact financier :** 5 800 comptes ont été utilisés pour des transactions non autorisées, engendrant 250 000 $ de pertes directes (incluant les rétrofacturations).
*   **Monétisation :** Les données volées étaient traitées et revendues via des ressources en ligne et des bots Telegram. Le suspect utilisait également des plateformes d'échange de cryptomonnaies pour blanchir les gains.
*   **Technique avancée :** Le vol de jetons de session permet aux attaquants de contourner les mécanismes d'authentification multifacteur (MFA) en accédant directement aux sessions actives des victimes.

**Vulnérabilités :**
L'article ne mentionne pas de CVE spécifique, car l'attaque repose sur l'infection initiale des postes clients par des malwares volant des données sensibles déjà authentifiées (cookies/jetons de session), rendant les contrôles d'authentification classiques inopérants.

**Recommandations :**
*   **Sécurisation des endpoints :** Utiliser des solutions EDR/antivirus robustes pour détecter et bloquer l'exécution de logiciels de type *infostealer*.
*   **Gestion des sessions :** Réduire la durée de vie des jetons de session et mettre en œuvre des politiques de déconnexion automatique en cas d'inactivité.
*   **Surveillance des anomalies :** Détecter les changements suspects d'adresses IP ou de "User-Agent" lors des sessions utilisateur pour identifier une usurpation de jeton.
*   **Hygiène numérique :** Sensibiliser les utilisateurs aux risques de téléchargement de logiciels tiers et à l'importance de ne pas enregistrer de données critiques (mots de passe, moyens de paiement) directement dans le navigateur.

---
[Source](https://www.bleepingcomputer.com/news/security/ukraine-identifies-infostealer-operator-tied-to-28-000-stolen-accounts/){:target="_blank"}
