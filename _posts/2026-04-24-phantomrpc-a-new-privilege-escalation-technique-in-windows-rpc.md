---
title: 'PhantomRPC: A new privilege escalation technique in Windows RPC'
date: 2026-04-24
permalink: /posts/2026/04/24/phantomrpc-a-new-privilege-escalation-technique-in-windows-rpc/
tags:
- veille-cyber
- securelist
---
### PhantomRPC : Vulnérabilité d'élévation de privilèges via l'architecture RPC de Windows

**Points clés**
*   **Vulnérabilité architecturale :** Le mécanisme RPC (Remote Procedure Call) de Windows ne vérifie pas l'authenticité des serveurs RPC. Il permet à un attaquant de déployer un serveur RPC malveillant sur un point de terminaison (endpoint) attendu mais inactif, interceptant ainsi les requêtes des processus légitimes.
*   **Mécanisme d'exploitation :** Lorsqu'un service système tente de se connecter à un serveur RPC indisponible, le client RPC peut se connecter à l'implémentation malveillante de l'attaquant. Si la requête RPC utilise un niveau d'impersonation élevé (Impersonate), l'attaquant peut invoquer `RpcImpersonateClient` pour usurper l'identité du processus client (souvent SYSTEM).
*   **Prérequis :** L'attaquant doit déjà disposer du privilège `SeImpersonatePrivilege` (généralement détenu par les comptes *Network Service* ou *Local Service*) pour réussir l'élévation de privilèges.
*   **Impact :** Élévation de privilèges locaux vers SYSTEM ou administrateur. Cinq vecteurs d'attaque ont été identifiés, allant de la coercition de services (ex: *gpupdate*) à l'attente d'interactions utilisateur ou de tâches de fond.

**Vulnérabilités**
*   **CVE :** Aucune. Microsoft a classé cette faille comme une vulnérabilité de sévérité "modérée", estimant que l'exigence du privilège `SeImpersonatePrivilege` limite suffisamment le risque pour ne pas justifier un correctif immédiat ou une attribution de CVE.

**Recommandations**
*   **Monitoring :** Utiliser les outils de suivi ETW (Event Tracing for Windows) pour identifier les erreurs `RPC_S_SERVER_UNAVAILABLE` (Code 1722). Des comportements suspects peuvent indiquer qu'un processus tente de communiquer avec un service absent, créant une opportunité pour un serveur malveillant.
*   **Réduction de la surface d'attaque :**
    *   Activer les services critiques, même s'ils semblent inutilisés, afin d'occuper les points de terminaison RPC et empêcher le déploiement de serveurs frauduleux.
    *   Auditer et restreindre strictement l'octroi du privilège `SeImpersonatePrivilege` aux seuls processus qui en ont réellement besoin.
*   **Outils :** Le chercheur a mis à disposition un dépôt GitHub ([PhantomRPC](https://github.com/klsecservices/PhantomRPC)) contenant des scripts de détection et des preuves de concept pour aider les administrateurs à auditer leurs environnements.

---
[Source](https://securelist.com/phantomrpc-rpc-vulnerability/119428/){:target="_blank"}
