---
title: 'Microsoft to secure Entra ID sign-ins from script injection attacks'
date: 2025-11-26
permalink: /posts/2025/11/26/microsoft-to-secure-entra-id-sign-ins-from-script-injection-attacks/
tags:
- veille-cyber
- bleepingcomp
---
**Renforcement de la sécurité des connexions Entra ID contre les injections de scripts**

Microsoft va renforcer la sécurité du système d'authentification Entra ID contre les attaques par injection de scripts externes à partir de mi-octobre 2026. Une politique de sécurité du contenu (CSP) améliorée limitera l'exécution des scripts aux sources approuvées par Microsoft, protégeant ainsi contre les risques tels que le cross-site scripting (XSS) utilisé pour voler des identifiants. Cette mesure s'appliquera aux expériences de connexion basées sur navigateur et n'affectera pas Microsoft Entra External ID.

**Points clés :**

*   **Amélioration de la sécurité CSP :** Permettra l'exécution de scripts uniquement à partir de domaines de livraison de contenu et de sources inline fiables pour Microsoft pendant le processus de connexion.
*   **Protection contre le XSS :** Empêchera les attaquants d'injecter du code malveillant pour le vol d'informations d'identification ou la compromission de systèmes.
*   **Portée :** Concerne uniquement les connexions via le navigateur aux URL commençant par login.microsoftonline.com.
*   **Planification :** Le déploiement est prévu pour mi-à-fin octobre 2026.
*   **Initiative SFI :** Cette mise à jour s'inscrit dans le cadre de l'Initiative Secure Future (SFI) de Microsoft, visant à améliorer la posture de sécurité globale de l'entreprise.

**Vulnérabilités :**

*   **Injection de scripts externes :** Permet aux attaquants d'introduire du code non autorisé dans le processus de connexion.
*   **Cross-Site Scripting (XSS) :** Risque spécifique d'exécution de code malveillant pour l'exploitation des informations utilisateur.
*   *(Aucun CVE spécifique n'est mentionné dans l'article pour ces risques généraux liés à l'injection de scripts dans ce contexte précis.)*

**Recommandations :**

*   **Tests des scénarios de connexion :** Les organisations doivent tester leurs flux de connexion avant octobre 2026 pour identifier et résoudre toute dépendance à des outils d'injection de code.
*   **Identification des impacts :** Les administrateurs IT peuvent surveiller la console du développeur du navigateur pendant les connexions ; les violations apparaîtront en rouge.
*   **Cessation de l'utilisation d'extensions/outils d'injection de code :** Les clients d'entreprise sont invités à arrêter d'utiliser des extensions ou des outils de navigateur qui injectent des scripts dans les pages de connexion avant que le changement ne prenne effet, car ils ne seront plus pris en charge.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-to-secure-entra-id-sign-ins-from-external-script-injection-attacks/){:target="_blank"}
