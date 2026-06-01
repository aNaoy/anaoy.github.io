---
title: 'Hackers Used Meta’s AI Support Bot to Seize Instagram Accounts'
date: 2026-06-01
permalink: /posts/2026/06/01/hackers-used-metas-ai-support-bot-to-seize-instagram-accounts/
tags:
- veille-cyber
- krebs
---
### Détournement de comptes Instagram via l'IA de Meta

Des hackers ont exploité une faille dans l'assistant de support par intelligence artificielle de Meta pour pirater des comptes Instagram de premier plan, dont celui de la Maison-Blanche (sous l'ère Obama). En manipulant le bot via une procédure de réinitialisation de mot de passe, les attaquants parvenaient à lier une nouvelle adresse e-mail au compte cible pour en prendre le contrôle.

**Points clés**
*   **Mode opératoire :** Les attaquants utilisaient un VPN localisé à proximité de la position habituelle de la victime pour paraître légitimes. Ils demandaient à l'IA de lier un nouvel e-mail au compte, laquelle envoyait alors un code de validation permettant de réinitialiser le mot de passe.
*   **Motivation :** Outre le vandalisme à caractère politique, cette faille a été utilisée pour détourner des comptes « précieux » (noms d'utilisateurs courts) dont la valeur de revente est très élevée.
*   **Réponse de Meta :** L'entreprise a déployé un correctif d'urgence après les incidents. Aucune brèche dans les bases de données backend n'a été constatée.

**Vulnérabilités**
*   **Faille logique de l'IA :** Le bot de support automatisé manquait de contrôles de vérification suffisants pour confirmer l'identité réelle du demandeur avant de modifier les informations de récupération du compte. Aucun identifiant CVE n'a été attribué à ce jour, car il s'agit d'une erreur de conception de flux de travail.

**Recommandations**
*   **Activation de l'authentification multifacteur (MFA) :** L'activation de la MFA, même par SMS, constitue une protection efficace contre ce type d'exploitation, car les hackers ont confirmé que l'attaque échouait sur les comptes ainsi sécurisés.
*   **Utilisation de méthodes robustes :** Privilégier les clés de sécurité matérielles ou les applications d'authentification (passkeys) plutôt que les méthodes basées sur les SMS ou les e-mails, plus facilement détournables.
*   **Vigilance face aux bots de support :** Les plateformes doivent renforcer les garde-fous de leurs IA pour éviter qu'elles ne soient manipulables par ingénierie sociale automatisée.

---
[Source](https://krebsonsecurity.com/2026/06/hackers-used-metas-ai-support-bot-to-seize-instagram-accounts/){:target="_blank"}
