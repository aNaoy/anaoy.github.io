---
title: 'Cybercrime Groups Using Vishing and SSO Abuse in Rapid SaaS Extortion Attacks'
date: 2026-05-01
permalink: /posts/2026/05/01/cybercrime-groups-using-vishing-and-sso-abuse-in-rapid-saas-extortion-attacks/
tags:
- veille-cyber
- hackernews
---
### Menaces persistentes : L'essor des attaques SaaS par vishing et détournement d'authentification

Les groupes cybercriminels **Cordial Spider** et **Snarky Spider** mènent des campagnes d'extorsion rapides et à fort impact en ciblant exclusivement les environnements SaaS. Ces attaquants exploitent la confiance accordée aux fournisseurs d'identité (IdP) pour infiltrer l'ensemble de l'écosystème applicatif d'une entreprise sans avoir à compromettre chaque application individuellement.

**Points clés :**
*   **Techniques d'ingénierie sociale :** Utilisation intensive du *vishing* (phishing vocal) en se faisant passer pour le support informatique pour récolter identifiants et codes MFA.
*   **Détournement d'authentification :** Emploi de pages d'hameçonnage "Adversary-in-the-Middle" (AiTM) pour intercepter les sessions en temps réel.
*   **Persistance furtive :** Enregistrement de nouveaux appareils, suppression des anciens et création de règles de messagerie pour masquer les alertes de sécurité liées à ces activités.
*   **Mouvement latéral :** Exploitation des relations d'approbation entre l'IdP et les services SaaS (Google Workspace, HubSpot, SharePoint, Salesforce) pour un accès illimité.
*   **Evasion :** Usage de proxys résidentiels pour contourner les filtrages IP et techniques de type "Living-off-the-Land" (LotL).

**Vulnérabilités :**
*   L'article ne mentionne pas de CVE spécifique, car les attaques reposent sur l'abus de fonctionnalités légitimes de gestion des identités et sur la vulnérabilité humaine face au *vishing*, plutôt que sur des failles logicielles exploitables via des vulnérabilités connues.

**Recommandations :**
*   **Renforcement de l'authentification :** Privilégier les clés de sécurité physiques ou les méthodes d'authentification résistantes au phishing (FIDO2) plutôt que les codes MFA basés sur SMS ou applications mobiles vulnérables aux interceptions AiTM.
*   **Monitoring des accès :** Surveiller étroitement l'enregistrement de nouveaux appareils et la modification des règles de transfert ou de suppression automatique des emails dans les messageries d'entreprise.
*   **Politiques de sécurité SaaS :** Restreindre les privilèges des comptes IdP et mettre en place une surveillance renforcée sur les accès aux données critiques dans les applications SaaS.
*   **Sensibilisation :** Former spécifiquement les employés aux risques d'appels téléphoniques non sollicités prétendant provenir du service informatique.

---
[Source](https://thehackernews.com/2026/05/cybercrime-groups-using-vishing-and-sso.html){:target="_blank"}
