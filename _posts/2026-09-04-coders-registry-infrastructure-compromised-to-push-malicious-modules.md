---
title: 'Coders registry infrastructure compromised to push malicious modules'
date: 2026-09-04
permalink: /posts/2026/09/04/coders-registry-infrastructure-compromised-to-push-malicious-modules/
tags:
- veille-cyber
- bleepingcomp
---
### Compromission de l'infrastructure Cloudflare de Coder : Distribution de modules malveillants

Des attaquants ont compromis l'infrastructure Cloudflare de Coder, plateforme utilisée pour les environnements de développement cloud, en ajoutant des serveurs non autorisés au registre de modules Terraform. Entre le 31 août, de 07h35 à 21h45 UTC, ces serveurs ont servi des modules modifiés capables de dérober des identifiants sensibles et de les exfiltrer vers le domaine `coder-infra[.]com`.

**Points clés :**
*   **Cible :** Utilisateurs de la plateforme Coder ayant téléchargé des modules Terraform durant la fenêtre d'exposition.
*   **Méthode :** Injection d'adresses IP malveillantes dans le pool de serveurs du registre `registry.coder.com`.
*   **Objectif :** Vol de secrets (clés API cloud/IA, variables d'environnement, jetons OIDC, clés SSH, identifiants CI/CD, historiques de terminal).
*   **Impact :** Bien que l'exfiltration ait eu lieu, aucun impact direct sur les données hébergées par Coder n'a été constaté. L'impossibilité d'accéder aux logs de l'attaquant empêche toutefois une identification exhaustive des victimes.

**Vulnérabilités :**
*   Aucune CVE spécifique n'a été attribuée, car l'attaque résulte d'une compromission de l'infrastructure réseau (Cloudflare) plutôt que d'une faille logicielle directe dans le code de Coder.

**Recommandations :**
*   **Rotation immédiate :** Renouveler tous les secrets, clés API, clés SSH et jetons potentiellement exposés sur les hôtes ayant utilisé le registre durant la période concernée.
*   **Analyse forensique :**
    *   Rechercher dans les logs (pare-feu, proxy, DNS, VPC) toute trace de connexion vers le domaine `coder-infra[.]com`.
    *   Inspecter les logs des provisionneurs à la recherche de requêtes `data.external.telemetry`.
*   **Nettoyage :** Identifier et purger les modules malveillants éventuellement mis en cache. Coder a mis à disposition une requête SQL pour aider à identifier les versions de modules affectées.
*   **Mise à jour :** Appliquer les correctifs fournis par Coder (versions 2.37.0, 2.36.4, 2.35.7 et 2.34.9).

---
[Source](https://www.bleepingcomputer.com/news/security/coders-registry-infrastructure-compromised-to-push-malicious-modules/){:target="_blank"}
