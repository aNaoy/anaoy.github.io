---
title: 'Robinhood account creation flaw abused to send phishing emails'
date: 2026-04-28
permalink: /posts/2026/04/28/robinhood-account-creation-flaw-abused-to-send-phishing-emails/
tags:
- veille-cyber
- bleepingcomp
---
### Faille dans le processus d'inscription de Robinhood détournée pour du phishing

Des attaquants ont exploité une vulnérabilité dans le processus de création de compte de la plateforme Robinhood pour envoyer des courriels de phishing hautement crédibles, semblant provenir de l'adresse officielle `noreply@robinhood.com` et passant avec succès les vérifications SPF/DKIM.

**Points clés :**
* **Méthode d'attaque :** Les pirates ont utilisé des listes d'adresses électroniques provenant de fuites de données antérieures. Ils ont créé des comptes Robinhood en utilisant des variantes d'alias (dot aliasing) pour cibler les clients réels.
* **Technique d'injection :** Les attaquants ont inséré du code HTML arbitraire dans les champs de métadonnées des appareils lors de l'inscription. Cette injection était ensuite intégrée automatiquement par Robinhood dans les courriels de notification de connexion légitimes.
* **Conséquences :** Les courriels contenaient un message d'alerte factice sur une "activité suspecte" incitant les utilisateurs à cliquer sur un lien menant vers un site frauduleux destiné à dérober leurs identifiants.
* **Réponse de Robinhood :** La société a confirmé l'incident, précisant qu'il ne s'agissait pas d'une violation de ses systèmes de sécurité internes ou des comptes utilisateurs, mais d'un abus de son processus d'onboarding.

**Vulnérabilités :**
* Absence de désinfection (sanitization) des entrées utilisateur dans les champs de métadonnées d'appareil lors du processus d'inscription. (Aucune CVE spécifique n'a été attribuée à ce jour).

**Recommandations :**
* **Pour l'entreprise :** Robinhood a déjà corrigé la faille en supprimant le champ "Device" des courriels de confirmation de création de compte.
* **Pour les utilisateurs :** Supprimer immédiatement les courriels suspects reçus et ne cliquer sur aucun lien contenu dans ces messages. En cas de doute, se rendre directement sur le site officiel via son navigateur habituel.

---
[Source](https://www.bleepingcomputer.com/news/security/robinhood-account-creation-flaw-abused-to-send-phishing-emails/){:target="_blank"}
