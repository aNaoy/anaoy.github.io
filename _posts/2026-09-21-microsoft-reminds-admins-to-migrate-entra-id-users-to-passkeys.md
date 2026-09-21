---
title: 'Microsoft reminds admins to migrate Entra ID users to passkeys'
date: 2026-09-21
permalink: /posts/2026/09/21/microsoft-reminds-admins-to-migrate-entra-id-users-to-passkeys/
tags:
- veille-cyber
- bleepingcomp
---
### Fin de l'authentification par SMS sur Microsoft Entra ID

Microsoft annonce l'arrêt définitif de l'authentification par SMS et par appel vocal comme méthode de connexion de premier facteur pour les utilisateurs de Microsoft Entra ID à partir du 1er février 2027. Cette mesure vise à renforcer la sécurité face aux risques croissants d'hameçonnage (phishing), de fraude et de compromission de comptes liés à ces méthodes obsolètes.

**Points clés**
*   **Transition imposée :** Les méthodes d'authentification par SMS ou voix seront désactivées, même pour les entreprises utilisant des fournisseurs de téléphonie tiers.
*   **Adoption des passkeys :** Microsoft déploie progressivement les *passkeys* comme méthode d'authentification par défaut. Les utilisateurs seront automatiquement invités à enregistrer une *passkey* lors de leur prochaine authentification multi-facteurs (MFA).
*   **Périmètre :** La mesure concerne les environnements de travail (workforce tenants) et ne touche pas les scénarios Azure AD B2C ou Microsoft Entra External ID.
*   **Outil de diagnostic :** Un script PowerShell (Entra SMS/Voice Policy Scanner) est disponible pour permettre aux administrateurs d'identifier les utilisateurs utilisant encore l'authentification par SMS ou voix.

**Vulnérabilités associées**
Bien qu'aucune CVE spécifique ne soit mentionnée, l'article souligne une vulnérabilité structurelle liée à l'utilisation des méthodes SMS et voix :
*   **Sensibilité au phishing et à l'interception :** Ces méthodes ne sont pas résistantes à l'hameçonnage, exposant les comptes à des risques élevés de piratage.

**Recommandations pour les administrateurs**
*   **Anticiper la migration :** Planifier la transition des utilisateurs vers des méthodes résistantes à l'hameçonnage avant l'échéance de février 2027.
*   **Privilégier les alternatives modernes :** Déployer les *passkeys*, les clés de sécurité FIDO2 ou l'authentification par QR code.
*   **Auditer les usages :** Utiliser le script fourni par Microsoft sur GitHub pour cartographier les utilisateurs dépendant encore des méthodes basées sur le téléphone.
*   **Configuration tierce :** Pour les organisations nécessitant absolument l'authentification par téléphone, il est impératif de configurer des fournisseurs de télécom tiers via le Microsoft Security Store avant la date limite.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-reminds-admins-to-migrate-entra-id-users-to-passkeys/){:target="_blank"}
