---
title: 'Critical RSC Bugs in React and Next.js Allow Unauthenticated Remote Code Execution'
date: 2025-12-03
permalink: /posts/2025/12/03/critical-rsc-bugs-in-react-and-nextjs-allow-unauthenticated-remote-code-execution/
tags:
- veille-cyber
- hackernews
---
**Exécution de code à distance critique dans React et Next.js**

Des failles de sécurité critiques ont été découvertes dans les React Server Components (RSC), permettant une exécution de code à distance non authentifiée.

**Points clés:**

*   Ces vulnérabilités exploitent la manière dont React décode les charges utiles envoyées aux points de terminaison des fonctions serveur React.
*   Même les applications qui n'implémentent pas directement de fonctions serveur React peuvent être vulnérables si elles utilisent des composants serveur React.
*   L'impact peut aller jusqu'à l'exécution de code JavaScript arbitraire sur le serveur.
*   Environ 39% des environnements cloud pourraient être concernés.

**Vulnérabilités:**

*   **CVE-2025-55182:** Concerne les paquets npm `react-server-dom-webpack`, `react-server-dom-parcel`, et `react-server-dom-turbopack` dans les versions 19.0, 19.1.0, 19.1.1, et 19.2.0. Score CVSS de 10.0.
*   **CVE-2025-66478:** Concerne Next.js utilisant App Router dans les versions >=14.3.0-canary.77, >=15, et >=16. Score CVSS de 10.0.

D'autres librairies utilisant RSC peuvent également être affectées.

**Recommandations:**

Il est fortement conseillé d'appliquer les mises à jour dès que possible pour se protéger contre ces menaces.

*   Pour `react-server-dom-webpack`, `react-server-dom-parcel`, et `react-server-dom-turbopack`, mettez à jour vers les versions 19.0.1, 19.1.2, ou 19.2.1.
*   Pour Next.js, mettez à jour vers les versions patchées : 16.0.7, 15.5.7, 15.4.8, 15.3.6, 15.2.6, 15.1.9, ou 15.0.5.

---
[Source](https://thehackernews.com/2025/12/critical-rsc-bugs-in-react-and-nextjs.html){:target="_blank"}
