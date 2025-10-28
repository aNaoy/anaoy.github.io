---
title: 'Italian spyware vendor linked to Chrome zero-day attacks'
date: 2025-10-28
permalink: /posts/2025/10/28/italian-spyware-vendor-linked-to-chrome-zero-day-attacks/
tags:
- veille-cyber
- bleepingcomp
---
**L'ombre de Hacking Team plane sur une campagne d'espionnage**

Une campagne d'espionnage nommée "Operation ForumTroll" a exploité une faille de sécurité critique (zero-day) dans le navigateur Google Chrome pour distribuer un logiciel espion sophistiqué. Cette vulnérabilité, identifiée comme CVE-2025-2783, permettait à distance l'exécution de code et l'évasion du bac à sable du navigateur. L'attaque visait spécifiquement des organisations russes, incluant des médias, des universités, des centres de recherche, des entités gouvernementales et des institutions financières, via des invitations piégées à un forum.

L'analyse du logiciel malveillant utilisé a révélé des similitudes frappantes avec des outils développés par Memento Labs, une société italienne formée à partir des actifs de l'ancien vendeur de logiciels espions, Hacking Team. Hacking Team, connu pour son système de contrôle à distance (RCS) vendu à des autorités pour la surveillance, avait été victime d'une violation de données majeure en 2015. En 2019, la société a été acquise par InTheCyber Group, qui a ensuite utilisé ses ressources pour fonder Memento Labs.

Le logiciel espion au cœur de cette campagne est nommé "Dante", identifié comme un logiciel espion commercial. Les chercheurs ont également découvert l'utilisation d'un autre logiciel malveillant modulaire, "LeetAgent", qui présente des particularités dans l'implémentation de ses commandes utilisant le "leetspeak". Des attaques antérieures remontant à 2022 contre des cibles en Russie et en Biélorussie ont également été liées à LeetAgent, qui dans certains cas, servait à déployer Dante. La similarité du code de Dante avec le RCS de Hacking Team conforte l'attribution à Memento Labs.

**Points Clés :**

*   **Attaque Zero-Day :** Exploitation d'une vulnérabilité inconnue dans Chrome (CVE-2025-2783) pour installer des logiciels malveillants.
*   **Cible :** Organisations russes (médias, universités, gouvernement, finances).
*   **Méthode :** Phishing via des invitations à un forum contenant des liens malveillants.
*   **Logiciel Malveillant :** "Dante" (logiciel espion commercial) et "LeetAgent" (charge utile modulaire).
*   **Attribution :** Liens forts avec Memento Labs, une société issue de Hacking Team.

**Vulnérabilités :**

*   **CVE-2025-2783 :** Vulnérabilité de type "sandbox escape" dans Google Chrome.

**Recommandations :**

*   Maintenir les navigateurs web, notamment Google Chrome, à jour pour bénéficier des correctifs de sécurité. Google a corrigé CVE-2025-2783 dans la version 134.0.6998.178.
*   Appliquer les mises à jour de sécurité pour d'autres navigateurs affectés, comme Firefox qui a corrigé une vulnérabilité similaire (CVE-2025-2857) dans sa version 136.0.4.
*   Être vigilant face aux emails de phishing, même s'ils semblent personnalisés ou proviennent de sources potentiellement légitimes. Ne pas cliquer sur les liens suspects.

---
[Source](https://www.bleepingcomputer.com/news/security/italian-spyware-vendor-linked-to-chrome-zero-day-attacks/){:target="_blank"}
