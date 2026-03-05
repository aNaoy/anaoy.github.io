---
title: 'Europol-coordinated action disrupts Tycoon2FA phishing platform'
date: 2026-03-05
permalink: /posts/2026/03/05/europol-coordinated-action-disrupts-tycoon2fa-phishing-platform/
tags:
- veille-cyber
- bleepingcomp
---
### Démantèlement d'une Plateforme de Phishing Sophistiquée

Une opération internationale coordonnée par Europol a permis de démanteler Tycoon2FA, une plateforme majeure de phishing-as-a-service (PhaaS). Cette action, soutenue par des partenaires privés tels que Microsoft et Trend Micro, a entraîné la saisie et la mise hors ligne de 330 domaines constituant l'infrastructure de ce service criminel.

**Points Clés :**

*   **Magnitude :** Tycoon2FA était responsable de l'envoi de dizaines de millions de messages de phishing chaque mois, ciblant près de 100 000 organisations à travers le monde, y compris des institutions gouvernementales, des écoles et des établissements de santé.
*   **Mode Opératoire :** La plateforme fonctionnait comme un système "adversary-in-the-middle" (AITM), utilisant un serveur proxy inversé pour intercepter en temps réel les identifiants de connexion et les cookies de session des victimes.
*   **Contournement de la MFA :** Tycoon2FA permettait aux cybercriminels de détourner les protections de l'authentification multifacteur (MFA) en relayant les codes d'authentification à travers ses serveurs, tout en accédant aux sessions authentifiées.
*   **Accessibilité :** Proposé à bas prix sur Telegram, Tycoon2FA a abaissé le seuil d'entrée pour les cybercriminels peu qualifiés, leur permettant de mener des attaques sophistiquées à grande échelle.

**Vulnérabilités :**

Bien qu'aucun CVE spécifique ne soit mentionné pour la plateforme elle-même, son fonctionnement repose sur l'exploitation des processus d'authentification standard, permettant de :

*   Intercepter les identifiants de connexion.
*   Détourner les cookies de session actifs.
*   Relayer les codes d'authentification multifacteur (MFA) pour contourner cette couche de sécurité.

**Recommandations :**

*   **Révocation des sessions actives :** Les organisations ciblées par Tycoon2FA doivent explicitement révoquer les sessions actives et les jetons d'authentification, même après une réinitialisation de mot de passe, pour empêcher la persistance des attaquants.
*   **Surveillance des infrastructures :** La collaboration public-privé et le partage d'informations sont cruciaux pour identifier et perturber les infrastructures criminelles.

---
[Source](https://www.bleepingcomputer.com/news/security/europol-coordinated-action-disrupts-tycoon2fa-phishing-platform/){:target="_blank"}
