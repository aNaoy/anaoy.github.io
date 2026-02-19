---
title: 'Hackers target Microsoft Entra accounts in device code vishing attacks'
date: 2026-02-19
permalink: /posts/2026/02/19/hackers-target-microsoft-entra-accounts-in-device-code-vishing-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Campagne de Phishing Vishing Exploitant le Flux d'Autorisation d'Appareil Microsoft

Une nouvelle tactique de piratage cible les organisations des secteurs de la technologie, de la fabrication et de la finance. Elle combine le phishing par code d'appareil et le vishing (phishing vocal) pour exploiter le flux d'autorisation d'appareil OAuth 2.0 de Microsoft Entra. Contrairement aux attaques précédentes qui utilisaient des applications OAuth malveillantes, ces campagnes s'appuient sur des identifiants clients OAuth légitimes de Microsoft et le flux d'autorisation d'appareil pour tromper les victimes.

**Fonctionnement de l'attaque :**

1.  **Appât Vishing :** Les attaquants contactent des employés ciblés, se faisant passer pour des entités légitimes, et les incitent à visiter une page de connexion Microsoft (microsoft.com/devicelogin).
2.  **Code d'Appareil :** Ils demandent ensuite à la victime d'entrer un code généré ("user\_code") sur cette page, prétendument pour connecter un appareil ou une application.
3.  **Authentification Légitime :** La victime saisit ses identifiants Microsoft Entra et effectue les vérifications MFA nécessaires, croyant authentifier un appareil légitime.
4.  **Obtention de Tokens :** Une fois authentifiée, le pirate, utilisant un identifiant client OAuth légitime (potentiellement celui de Microsoft), peut récupérer un jeton d'actualisation ("refresh token") lié au compte de la victime. Ce jeton est ensuite échangé contre des jetons d'accès ("access tokens").
5.  **Accès sans MFA :** Ces jetons d'accès permettent aux attaquants de s'authentifier en tant qu'utilisateur dans Microsoft Entra et d'accéder aux applications SaaS connectées via l'authentification unique (SSO) du locataire victime, sans avoir besoin d'une nouvelle authentification MFA.

Cette méthode contourne les défenses traditionnelles en utilisant des flux d'authentification légitimes et évite la nécessité de voler des mots de passe ou d'intercepter des codes MFA directement. Les attaquants peuvent ainsi accéder aux données de l'entreprise et les utiliser à des fins d'extorsion.

La campagne est soupçonnée d'être menée par le groupe ShinyHunters, qui a déjà été lié à des attaques similaires contre les comptes Okta et Microsoft Entra.

**Points Clés :**

*   **Exploitation du flux d'autorisation d'appareil OAuth 2.0 :** Les attaquants abusent d'une fonctionnalité légitime conçue pour faciliter la connexion d'appareils à entrée limitée.
*   **Utilisation d'identifiants clients OAuth légitimes :** Ils n'ont pas besoin de créer d'applications malveillantes, augmentant la légitimité de l'apparence de l'attaque.
*   **Contournement de la MFA :** Une fois le premier accès obtenu via le flux, les jetons d'accès permettent des connexions ultérieures sans nouveau contrôle MFA.
*   **Accès aux applications SSO :** Permet d'accéder à une large gamme de services connectés (Microsoft 365, Salesforce, Google Workspace, etc.).

**Vulnérabilités :**

*   **Flux d'autorisation d'appareil OAuth 2.0 :** Bien que légitime, il peut être détourné par des attaques de social engineering.
*   Aucune CVE spécifique n'est mentionnée dans l'article pour cette technique.

**Recommandations :**

*   **Bloquer les domaines et adresses d'expéditeurs malveillants.**
*   **Auditer et révoquer les consentements d'applications OAuth suspectes.**
*   **Examiner les journaux de connexion Azure AD** pour détecter les événements d'authentification par code d'appareil.
*   **Désactiver l'option de flux de code d'appareil** si elle n'est pas strictement nécessaire.
*   **Mettre en œuvre des politiques d'accès conditionnel strictes.**

---
[Source](https://www.bleepingcomputer.com/news/security/hackers-target-microsoft-entra-accounts-in-device-code-vishing-attacks/){:target="_blank"}
