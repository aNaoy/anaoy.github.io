---
title: 'MFA Prompt Bombing: Why Your Second Factor Isnt Saving You'
date: 2026-05-26
permalink: /posts/2026/05/26/mfa-prompt-bombing-why-your-second-factor-isnt-saving-you/
tags:
- veille-cyber
- hackernews
---
### La menace du "MFA Prompt Bombing" : limites de l'authentification par notification push

Le "MFA Prompt Bombing" (ou fatigue MFA) est une technique où les attaquants, munis d'identifiants volés, déclenchent des notifications d'authentification répétées auprès de la cible jusqu'à ce que celle-ci finisse par valider l'accès, souvent par lassitude ou par confusion. Cette méthode est fréquemment couplée à du "vishing" (ingénierie sociale par téléphone), comme lors de l'attaque contre Cisco en 2022, où l'attaquant a réussi à obtenir un accès VPN en se faisant passer pour le support informatique.

**Points clés :**
*   **Vulnérabilité contextuelle :** Les notifications push classiques manquent d'informations (localisation, appareil, contexte), ce qui empêche l'utilisateur de distinguer une demande légitime d'une tentative frauduleuse.
*   **Chaîne d'attaque :** L'attaque repose sur trois piliers : des identifiants valides (issus de fuites), l'utilisation du MFA par notification push, et l'interaction humaine.
*   **Persistance :** Une fois l'accès initial obtenu, l'attaquant peut inscrire ses propres appareils au MFA pour maintenir son accès et escalader ses privilèges.

**Vulnérabilités :**
*   Le principal vecteur est la faiblesse intrinsèque des systèmes de **MFA basés sur les notifications push**, qui ne sont pas résistants au phishing ni à la fatigue de l'utilisateur. Aucune CVE spécifique n'est citée, car il s'agit d'une exploitation de la logique de conception des systèmes MFA et non d'une faille logicielle isolée.

**Recommandations :**
1.  **Adopter des facteurs MFA résistants :** Privilégier les méthodes insensibles à la fatigue, telles que les clés de sécurité FIDO2 (YubiKey), les jetons matériels ou le "number matching" (validation par saisie d'un code affiché).
2.  **Assainir les mots de passe :** Auditer et bloquer systématiquement les mots de passe compromis dans l'Active Directory pour empêcher l'attaquant d'initier la procédure MFA.
3.  **Appliquer des politiques d'accès conditionnel :** Introduire des signaux de risque en temps réel (géolocalisation, posture de l'appareil, comportement) pour bloquer automatiquement les tentatives suspectes avant même l'envoi d'une notification.

---
[Source](https://thehackernews.com/2026/05/mfa-prompt-bombing-why-your-second.html){:target="_blank"}
