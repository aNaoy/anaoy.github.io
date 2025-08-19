---
title: 'Amazon Q Developer: Secrets Leaked via DNS and Prompt Injection'
date: 2025-08-19
permalink: /posts/2025/08/19/amazon-q-developer-secrets-leaked-via-dns-and-prompt-injection/
tags:
- veille-cyber
- zerodaysfans
---
## Fuite de Secrets via Injection de Prompt dans Amazon Q Developer

L'extension VS Code d'Amazon Q Developer, utilisée par plus d'un million de développeurs, présentait une vulnérabilité critique permettant la fuite d'informations sensibles, telles que des clés API, vers des serveurs externes via des requêtes DNS. Cette faille pouvait être exploitée lors d'une attaque par injection de prompt indirecte.

### Points Clés

*   **Injection de Prompt :** L'outil pouvait être détourné pour exécuter des commandes shell et exfiltrer des données sans le consentement du développeur lorsqu'il interagissait avec des données non fiables.
*   **Exfiltration de Données via DNS :** Des commandes comme `ping` et `dig`, considérées comme "en lecture seule" par l'outil, permettaient d'envoyer des informations sensibles encodées dans des noms de domaine DNS.
*   **Attaque "Lethal Trifecta" :** La vulnérabilité illustre la combinaison d'une injection de prompt, d'une commande exécutable et d'une exfiltration de données.
*   **Contournement des protections :** L'outil refusait initialement les requêtes vers des domaines connus pour le testing de sécurité (comme `oast.me`), mais acceptait celles vers des domaines arbitraires (comme `wuzzi.net`), facilitant ainsi l'exfiltration.

### Vulnérabilités

*   **Type :** Injection de prompt, exfiltration de données.
*   **Impact :** Fuite de secrets (clés API, contenu de fichiers `.env`).
*   **CVE :** Aucune CVE n'est mentionnée dans l'article pour cette vulnérabilité spécifique.

### Recommandations

*   **Mise à Jour Immédiate :** Les utilisateurs doivent s'assurer d'exécuter la dernière version de l'extension Amazon Q Developer, car la faille a été corrigée par Amazon.
*   **Validation Humaine :** Une recommandation suggère d'implémenter une validation "human-in-the-loop" pour les commandes potentiellement dangereuses, comme `ping` et `dig`, en les retirant de la liste des commandes autorisées par défaut.

Amazon a corrigé cette vulnérabilité de manière discrète, sans émettre d'avis de sécurité public ni de CVE, ce qui est noté comme un manque par rapport aux pratiques industrielles courantes en matière de divulgation responsable.

---
[Source](https://embracethered.com/blog/posts/2025/amazon-q-developer-data-exfil-via-dns/){:target="_blank"}
