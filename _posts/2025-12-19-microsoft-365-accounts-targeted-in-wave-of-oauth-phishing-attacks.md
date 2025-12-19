---
title: 'Microsoft 365 accounts targeted in wave of OAuth phishing attacks'
date: 2025-12-19
permalink: /posts/2025/12/19/microsoft-365-accounts-targeted-in-wave-of-oauth-phishing-attacks/
tags:
- veille-cyber
- bleepingcomp
---
## Piratage de comptes Microsoft 365 via des attaques OAuth

Des acteurs malveillants multiplient les attaques de phishing visant les comptes Microsoft 365 en exploitant le mécanisme d'autorisation de code d'appareil OAuth. Ces attaques, bien que non nouvelles, ont vu leur volume augmenter de manière significative depuis septembre 2025, impliquant des cybercriminels à motivation financière ainsi que des groupes étatiques.

Les méthodes utilisées consistent à tromper les victimes pour qu'elles saisissent un code d'appareil sur une page de connexion Microsoft légitime. Ce faisant, elles autorisent involontairement une application contrôlée par l'attaquant, lui accordant ainsi un accès au compte cible sans nécessiter le vol d'identifiants ni contourner l'authentification multifacteur (MFA).

Deux kits de phishing ont été identifiés : SquarePhish (v1 et v2) et Graphish. SquarePhish est un outil de "red teaming" disponible publiquement, ciblant les flux d'autorisation via des codes QR. Graphish, un kit de phishing malveillant partagé sur des forums, prend en charge l'abus d'OAuth, les enregistrements d'applications Azure et les attaques "adversary-in-the-middle" (AiTM).

Trois campagnes notables ont été observées :

*   **Attaques "Bonus Salarial"** : Utilisation de leurres de partage de documents et de marquages d'entreprise localisés pour inciter les victimes à cliquer sur des liens menant à des sites contrôlés par les attaquants. Les victimes sont ensuite invitées à effectuer une "authentification sécurisée" en saisissant un code sur la page de connexion Microsoft.
*   **Attaques TA2723** : Cet acteur, déjà connu pour des campagnes de phishing d'identifiants ciblant OneDrive, LinkedIn et DocuSign, a commencé à utiliser le phishing par code d'appareil OAuth en octobre. Les premières phases auraient utilisé SquarePhish2, avec un passage potentiel à Graphish.
*   **Activité Étatique Suspectée (UNK_AcademicFlare)** : Depuis septembre 2025, un acteur suspecté d'être lié à la Russie utilise l'autorisation de code d'appareil OAuth pour le piratage de comptes. Il utilise des comptes de messagerie gouvernementaux et militaires compromis pour établir un lien avant de partager des liens usurpant OneDrive et dirigeant les victimes vers le flux de phishing. Ces attaques ciblent principalement les secteurs gouvernemental, académique, des groupes de réflexion et des transports aux États-Unis et en Europe.

Aucune vulnérabilité spécifique (CVE) n'est mentionnée dans l'article.

### Recommandations :

Pour contrer ces attaques, il est recommandé aux organisations d'utiliser Microsoft Entra Conditional Access dans la mesure du possible et d'envisager l'introduction d'une politique sur l'origine de la connexion.

---
[Source](https://www.bleepingcomputer.com/news/security/microsoft-365-accounts-targeted-in-wave-of-oauth-phishing-attacks/){:target="_blank"}
