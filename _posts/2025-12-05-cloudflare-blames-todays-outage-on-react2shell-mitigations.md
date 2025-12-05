---
title: 'Cloudflare blames todays outage on React2Shell mitigations'
date: 2025-12-05
permalink: /posts/2025/12/05/cloudflare-blames-todays-outage-on-react2shell-mitigations/
tags:
- veille-cyber
- bleepingcomp
---
**Problème mondial de Cloudflare lié à une faille React**

Un incident majeur a affecté la plateforme Cloudflare, provoquant des erreurs sur un grand nombre de sites web à travers le monde. La cause identifiée est l'implémentation d'une mesure d'urgence visant à corriger une vulnérabilité critique dans React Server Components.

**Points clés :**

*   L'incident n'a pas été causé par une cyberattaque, mais par une modification de la logique de traitement des requêtes de Cloudflare.
*   Environ 28 % du trafic HTTP géré par Cloudflare a été impacté.
*   La vulnérabilité corrigée est nommée "React2Shell" et est traquée sous la référence CVE-2025-55182.
*   Cette faille permet une exécution de code à distance dans les applications React et Next.js.
*   Plusieurs groupes de pirates informatiques chinois, ainsi que le NHS England, ont déjà exploité cette vulnérabilité.

**Vulnérabilités :**

*   **CVE-2025-55182 (React2Shell)** : Vulnérabilité d'exécution de code à distance dans React Server Components (RSC) affectant les versions de React 19.0, 19.1.0, 19.1.1 et 19.2.0.

**Recommandations :**

*   Les développeurs utilisant les composants React concernés doivent appliquer les correctifs disponibles.
*   Les organisations doivent rester vigilantes face à l'exploitation active de cette vulnérabilité.

---
[Source](https://www.bleepingcomputer.com/news/security/cloudflare-blames-todays-outage-on-emergency-react2shell-patch/){:target="_blank"}
