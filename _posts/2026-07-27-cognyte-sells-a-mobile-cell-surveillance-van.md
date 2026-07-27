---
title: 'Cognyte Sells a Mobile Cell Surveillance Van'
date: 2026-07-27
permalink: /posts/2026/07/27/cognyte-sells-a-mobile-cell-surveillance-van/
tags:
- veille-cyber
- schneier
---
### FalcoNet : La surveillance mobile par simulation d'antennes relais

L'entreprise israélienne Cognyte commercialise « FalcoNet », un système de surveillance mobile capable de simuler une antenne-relais. Ce dispositif contraint les téléphones portables situés à proximité à s'y connecter, permettant aux forces de l'ordre de suivre et d'identifier les appareils dans un périmètre donné, indépendamment de leur propriétaire.

**Points clés :**
*   **Technologie intrusive :** Le système fonctionne comme un « IMSI-catcher » (similaire au dispositif Stingray), captant les identifiants uniques des téléphones alentour.
*   **Polyvalence opérationnelle :** Le matériel est hautement adaptable ; il peut être intégré à des véhicules, dissimulé dans des sacs à dos pour des opérations pédestres ou monté sur des hélicoptères.
*   **Surveillance de masse :** La technologie ne cible pas uniquement les suspects, mais collecte potentiellement des données sur tous les citoyens présents dans la zone de couverture.

**Vulnérabilités :**
*   Il ne s'agit pas d'une vulnérabilité logicielle classifiée par une CVE, mais d'une **faille inhérente aux protocoles de communication mobile** (2G/3G/4G/5G). Ces protocoles permettent à un appareil non autorisé de se faire passer pour une station de base légitime (man-in-the-middle), trompant ainsi les téléphones mobiles.

**Recommandations :**
*   **Hygiène numérique :** Utiliser des applications de messagerie chiffrées de bout en bout pour protéger le contenu des communications, même si l'interception de l'identifiant matériel reste complexe à éviter.
*   **Protection matérielle :** Désactiver les connexions cellulaires (passage en mode avion) lorsque la sécurité des déplacements est une priorité absolue, ou utiliser des dispositifs sécurisés (type *Faraday bag*) pour bloquer tout signal radio.
*   **Sensibilisation :** Les utilisateurs doivent être conscients que la simple présence d'un téléphone allumé rend l'appareil vulnérable à la localisation par des tiers utilisant des simulateurs d'antennes-relais.

---
[Source](https://www.schneier.com/blog/archives/2026/07/cognyte-sells-a-mobile-cell-surveillance-van.html){:target="_blank"}
