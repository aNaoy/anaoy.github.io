---
title: 'Critical React, Next.js flaw lets hackers execute code on servers'
date: 2025-12-04
permalink: /posts/2025/12/04/critical-react-nextjs-flaw-lets-hackers-execute-code-on-servers/
tags:
- veille-cyber
- bleepingcomp
---
**Vulnérabilité Majeure dans React et Next.js : Exécution de Code à Distance Sans Authentification**

Une faille de sécurité critique, baptisée 'React2Shell', affectant le protocole 'Flight' des React Server Components (RSC) permet l'exécution de code à distance (RCE) sur les serveurs sans nécessiter d'authentification. Cette vulnérabilité, issue d'une désérialisation non sécurisée, a reçu la note de gravité maximale de 10/10.

**Points Clés :**

*   **Nature de la faille :** Désérialisation non sécurisée dans le protocole 'Flight' des React Server Components.
*   **Impact :** Permet à des attaquants d'exécuter du code arbitraire sur le serveur via des requêtes HTTP spécialement conçues vers les points d'accès React Server Function.
*   **Portée :** Affecte les applications React et Next.js utilisant les React Server Components, même si aucune React Server Function n'est explicitement implémentée.

**Vulnérabilités (avec CVE) :**

*   **React :** CVE-2025-55182
*   **Next.js :** CVE-2025-66478 (CVE rejeté dans la base de données nationale des vulnérabilités)

**Versions Affectées :**

*   **React :** Versions 19.0, 19.1.0, 19.1.1, et 19.2.0.
*   **Next.js :** Releases expérimentales canary à partir de 14.3.0-canary.77, ainsi que toutes les versions des branches 15.x et 16.x inférieures aux versions corrigées.
*   D'autres bibliothèques implémentant React Server, comme le plugin Vite RSC, le plugin Parcel RSC, React Router RSC preview, RedwoodSDK, et Waku, sont potentiellement affectées.

**Recommandations :**

*   **Mise à jour immédiate :** Appliquer les correctifs disponibles dans les versions suivantes :
    *   React : 19.0.1, 19.1.2, et 19.2.1.
    *   Next.js : 15.0.5, 15.1.9, 15.2.6, 15.3.6, 15.4.8, 15.5.7, et 16.0.7.
*   **Audit des environnements :** Vérifier l'utilisation de versions vulnérables dans les environnements de production et prendre les mesures d'atténuation appropriées.

---
[Source](https://www.bleepingcomputer.com/news/security/critical-react2shell-flaw-in-react-nextjs-lets-hackers-run-javascript-code/){:target="_blank"}
