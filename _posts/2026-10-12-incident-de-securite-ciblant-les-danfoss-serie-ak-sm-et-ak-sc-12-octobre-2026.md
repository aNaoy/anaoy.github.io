---
title: 'Incident de sécurité ciblant les Danfoss série AK-SM et AK-SC (12 octobre 2026)'
date: 2026-10-12
permalink: /posts/2026/10/12/incident-de-securite-ciblant-les-danfoss-serie-ak-sm-et-ak-sc-12-octobre-2026/
tags:
- veille-cyber
- certfr
---
### Alerte de compromission : contrôleurs Danfoss AK-SM et AK-SC

Le CERT-FR signale une vague de compromissions affectant les systèmes de gestion Danfoss des séries AK-SM et AK-SC exposés sur Internet.

**Points clés**
*   Les équipements sont la cible d'attaques actives suite à l'exposition de leurs interfaces d'administration.
*   L'accès direct via Internet est formellement déconseillé.

**Vulnérabilités**
*   Aucune CVE spécifique n'est mentionnée, la vulnérabilité principale réside dans l'exposition publique des interfaces de gestion.

**Recommandations**
*   **Action immédiate :** Déconnecter l'équipement d'Internet ou restreindre strictement l'accès via un filtrage IP (listes blanches).
*   **En cas de compromission suspectée :**
    *   Effectuer une réinitialisation complète aux paramètres d'usine (*Factory Reset*).
    *   Appliquer tous les correctifs de sécurité disponibles.
    *   Procéder à une rotation systématique des secrets (mots de passe, clés).
    *   Auditer l'ensemble des comptes utilisateurs présents sur le système.
    *   Reconfigurer intégralement l'équipement.

---
[Source](https://www.cert.ssi.gouv.fr/alerte/CERTFR-2026-ALE-012/){:target="_blank"}
