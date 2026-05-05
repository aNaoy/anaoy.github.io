---
title: 'The Danger of Multi-SSO AWS Cognito User Pools'
date: 2026-05-05
permalink: /posts/2026/05/05/the-danger-of-multi-sso-aws-cognito-user-pools/
tags:
- veille-cyber
- zerodaysfans
---
### Risques de sécurité dans les configurations Multi-SSO AWS Cognito

Les déploiements multi-locataires utilisant AWS Cognito avec plusieurs fournisseurs d'identité (IdP) externes présentent des vecteurs d'attaque spécifiques liés à la complexité des flux d'authentification et à la gestion des déclencheurs (triggers) Lambda.

#### Points clés
*   **Injection d'identité "fantôme" :** Un IdP malveillant peut créer des enregistrements utilisateurs persistants dans le pool si les contrôles de domaine ne sont pas appliqués strictement dans le trigger `PreSignUp_ExternalProvider`.
*   **Différentiels d'exécution :** Les contraintes de sécurité appliquées uniquement lors du premier login (via `PreSignUp`) ou uniquement lors des connexions suivantes (via `PreAuthentication`) créent des failles de sécurité.
*   **Manipulation de l'identifiant utilisateur :** Cognito génère des identifiants au format `ProviderName_sub`. Des attaquants peuvent exploiter des homoglyphes dans le nom du fournisseur ou injecter des underscores dans le champ `sub` pour contourner les parsers fragiles utilisant des index positionnels.
*   **Détournement de routage :** Si les `IdpIdentifiers` (utilisés pour rediriger les utilisateurs vers leur IdP) ne sont pas validés contre la propriété réelle du domaine par le locataire, un attaquant peut détourner le flux d'authentification vers un IdP malveillant.

#### Vulnérabilités (Aucun CVE spécifique attribué)
*   **Contournement de logique métier (Parser Differential) :** Erreurs lors de l'extraction de l'identité via `split("_")` permettant une élévation de privilèges ou une usurpation d'identité.
*   **Injections de métadonnées :** Manipulation du mapping d'attributs (`AttributeMapping`) pour injecter des attributs sensibles (ex: `custom:isAdmin`) via des fonctions JIT (Just-In-Time) provisioning.

#### Recommandations
*   **Centraliser les contrôles :** Appliquer les politiques de sécurité (vérification de domaine, etc.) dans le trigger `PreSignUp`, en le branchant explicitement sur toutes les sources d'événements (`PreSignUp_SignUp`, `PreSignUp_ExternalProvider`, `PreSignUp_AdminCreateUser`).
*   **Sécuriser le parsing :** Ne jamais utiliser de split positionnel sur `event.userName`. Préférer un `maxsplit=1` ou une normalisation stricte, partagée entre toutes les fonctions de sécurité.
*   **Validation des IdP :** Ne jamais exposer les `IdpIdentifiers` comme des champs libres dans une interface utilisateur. Assurer une vérification de propriété de domaine avant toute configuration.
*   **Isolation des attributs :** Ne pas mapper les attributs de sécurité (rôles, tenantID) directement depuis l'IdP externe. Les dériver côté serveur dans une Lambda de confiance.
*   **Audit des triggers :** Vérifier que les contrôles de sécurité ne reposent pas uniquement sur `PostAuthentication` (qui ne peut pas bloquer une session) et que chaque chaîne d'authentification est couverte de manière cohérente.

---
[Source](https://blog.doyensec.com/2026/05/05/cloudsectidbits-masso-cognito-sso.html){:target="_blank"}
