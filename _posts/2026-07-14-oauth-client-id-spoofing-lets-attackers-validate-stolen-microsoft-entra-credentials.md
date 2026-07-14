---
title: 'OAuth Client ID Spoofing Lets Attackers Validate Stolen Microsoft Entra Credentials'
date: 2026-07-14
permalink: /posts/2026/07/14/oauth-client-id-spoofing-lets-attackers-validate-stolen-microsoft-entra-credentials/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité par usurpation d'identifiant client OAuth dans Microsoft Entra ID

Une nouvelle technique d'usurpation d'identifiant client (OAuth Client ID Spoofing) permet aux attaquants de valider des identifiants volés et d'énumérer des comptes utilisateurs dans les environnements Microsoft Entra ID sans jamais déclencher d'événement de connexion réussie. Cette méthode exploite une faille dans la télémétrie de Microsoft : les réponses d'erreur (codes AADSTS) varient selon la validité de l'identifiant fourni, permettant aux attaquants de confirmer l'existence d'un compte et l'exactitude d'un mot de passe sans être détectés par les systèmes de surveillance habituels.

**Points clés :**
*   **Contournement de la détection :** L'utilisation d'identifiants clients fictifs (mais syntaxiquement valides) empêche l'enregistrement du nom de l'application dans les journaux de connexion, rendant inopérantes les alertes basées sur le suivi d'applications spécifiques.
*   **Flux ROPC détourné :** Les attaquants ciblent le point de terminaison OAuth 2.0 via le flux "Resource Owner Password Credentials" (ROPC).
*   **Évasion des politiques :** Cette technique contourne les stratégies d'accès conditionnel (Conditional Access) qui sont configurées pour s'appliquer à des applications spécifiques, car aucune application légitime n'est réellement ciblée.
*   **Campagnes observées :** Des groupes comme *UNK_pyreq2323* et *UNK_OutFlareAZ* ont déjà exploité cette faille à grande échelle, ciblant des millions de comptes via des infrastructures cloud (AWS, Cloudflare).

**Vulnérabilités :**
*   Il s'agit d'une faiblesse logique inhérente à la manière dont Microsoft Entra ID traite les erreurs d'authentification OAuth et journalise les tentatives avec des `client_id` invalides. **Aucun identifiant CVE n'a été attribué** à ce jour pour cette technique d'évasion.

**Recommandations :**
*   **Renforcer la surveillance :** Ne pas se limiter aux alertes basées sur les noms d'applications. Surveiller les pics de requêtes d'authentification présentant des champs "Application Name" vides ou des identifiants clients non enregistrés dans les journaux Entra.
*   **Limiter l'usage de ROPC :** Restreindre ou désactiver, dans la mesure du possible, l'utilisation du flux ROPC au sein de l'organisation, car celui-ci est privilégié par les attaquants pour le "password spraying".
*   **Détection comportementale :** Mettre en place des alertes sur des volumes anormaux de requêtes d'authentification provenant d'adresses IP uniques, même si elles utilisent des identifiants clients fragmentés et variés.
*   **Révision des politiques :** Puisque les politiques d'accès conditionnel basées sur les applications sont inefficaces contre cette menace, privilégier des stratégies basées sur le risque utilisateur ou sur l'emplacement géographique/réseau.

---
[Source](https://thehackernews.com/2026/07/oauth-client-id-spoofing-lets-attackers.html){:target="_blank"}
