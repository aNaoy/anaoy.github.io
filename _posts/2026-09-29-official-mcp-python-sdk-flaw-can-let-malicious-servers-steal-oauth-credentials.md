---
title: 'Official MCP Python SDK Flaw Can Let Malicious Servers Steal OAuth Credentials'
date: 2026-09-29
permalink: /posts/2026/09/29/official-mcp-python-sdk-flaw-can-let-malicious-servers-steal-oauth-credentials/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique dans le SDK Python MCP : Risque de vol d'identifiants OAuth

Une faille de sécurité identifiée dans le SDK officiel Model Context Protocol (MCP) pour Python permet à des serveurs MCP malveillants de détourner les identifiants OAuth d'applications clientes. En manipulant la configuration du service d'autorisation, un attaquant peut intercepter les secrets clients, codes d'autorisation et clés de preuve PKCE.

**Points clés :**
* **Mécanisme de l'attaque :** Le SDK ne vérifiait pas systématiquement l'adresse du serveur d'autorisation. Un serveur malveillant peut rediriger la requête d'authentification vers une infrastructure sous son contrôle.
* **Impact :** Vol de jetons d'accès héritant des permissions de l'application. Les secrets clients étant persistants, l'attaquant conserve un accès illimité jusqu'à leur révocation.
* **Vulnérabilité :** Aucune CVE n'a été assignée à ce jour (référencé sous `GHSA-qx49-fqc8-xw99`). Scores de dangerosité : 7.5 (M2M) et 6.5 (interactif).

**Recommandations :**
* **Mise à jour immédiate :** Passer aux versions **1.30.0** (branche 1.x) ou **2.2.0** (branche 2.x).
* **Configuration obligatoire :** Pour `ClientCredentialsOAuthProvider` et `PrivateKeyJWTOAuthProvider`, il est impératif d'ajouter explicitement le paramètre `issuer=` afin de verrouiller le service d'authentification attendu.
* **Nettoyage :** Effacer les enregistrements OAuth clients existants après la mise à jour.
* **Mesures de remédiation :** Si une connexion à un serveur non fiable a eu lieu, procéder immédiatement à la rotation des secrets clients et à la révocation des jetons existants auprès du fournisseur de service.
* **Migration :** Abandonner l'usage de `RFC7523OAuthClientProvider` (obsolète et non sécurisable).

---
[Source](https://thehackernews.com/2026/09/official-mcp-python-sdk-flaw-can-let.html){:target="_blank"}
