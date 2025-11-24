---
title: 'Conflicts between URL mapping and URL based access control., (Mon, Nov 24th)'
date: 2025-11-24
permalink: /posts/2025/11/24/conflicts-between-url-mapping-and-url-based-access-control-mon-nov-24th/
tags:
- veille-cyber
- sans-isc
---
## Confusion entre mappage d'URL et contrôle d'accès

Des vulnérabilités importantes sont régulièrement découvertes suite à l'utilisation simultanée de mappages d'URL (ou alias) et de contrôles d'accès basés sur les URL. Ces problèmes peuvent permettre à des acteurs malveillants d'exécuter du code arbitraire.

### Points Clés

*   Les applications exemptent souvent certaines URL de l'authentification (pages d'aide, réinitialisation de mot de passe).
*   Les serveurs web utilisent des directives pour mapper des URL à des fichiers (ex: `RewriteRule` dans Apache, `location` dans NGINX).
*   La configuration de ces mappages, si elle n'est pas correctement prise en compte par les règles de contrôle d'accès de l'application, peut mener à des failles.
*   Les développeurs Java semblent particulièrement affectés par ce type de problème.
*   L'utilisation incorrecte des expressions régulières dans les configurations de mappage d'URL aggrave le risque.

### Vulnérabilités

*   **Hitachi Vantara Pentaho Business Analytics Server**: Exploitation via la fin de l'URL `/require.js` qui contourne l'authentification, entraînant une injection de modèle dans le processus `ldapTreeNodeChildren`.
    *   **CVE-2022-43939**
    *   **CVE-2022-43769**

### Recommandations

*   Examiner attentivement toutes les instructions de remaniement d'URL (URL remapping) dans la configuration du serveur web.
*   Vérifier que ces remaniements ne contredisent pas les hypothèses relatives à l'authentification et au contrôle d'accès de l'application.
*   Être particulièrement prudent lors de l'utilisation d'expressions régulières, en vérifiant leur exactitude et l'utilisation d'ancres pour terminer les chaînes.

---
[Source](https://isc.sans.edu/diary/rss/32518){:target="_blank"}
