---
title: '‘Popa’ Botnet Linked to Publicly-Traded Israeli Firm'
date: 2026-06-18
permalink: /posts/2026/06/18/popa-botnet-linked-to-publicly-traded-israeli-firm/
tags:
- veille-cyber
- krebs
---
### Le botnet Popa : des boîtiers TV au service de l'extraction de données par IA

Le botnet **Popa**, composé de 1,5 à 2,5 millions d'adresses IP uniques quotidiennes, transforme des boîtiers Android TV bon marché et des applications de Smart TV en nœuds de "proxy résidentiels". Ces appareils permettent à des tiers de relayer du trafic Internet pour masquer leur origine réelle, facilitant ainsi la fraude publicitaire, le contournement de blocages et, surtout, le scraping massif de données pour l'entraînement d'IA.

**Points clés :**
*   **Lien avec Alarum Technologies :** Des chercheurs (Synthient, Qurium) associent le SDK Popa à **NetNut**, service de proxy opéré par la firme cotée en bourse Alarum Technologies.
*   **Mode opératoire :** Les utilisateurs installent des applications tierces (souvent liées à la piraterie de contenu ou des utilitaires gratuits) contenant un SDK malveillant. Ce dernier ouvre un tunnel de communication persistant vers le réseau proxy, sans consentement explicite dans la majorité des cas.
*   **Périmètre étendu :** Outre les boîtiers TV, le problème touche les téléviseurs LG (webOS) et Samsung (Tizen), ainsi que de nombreuses applications mobiles, infiltrant même les réseaux d'entreprises, bancaires et gouvernementaux.
*   **Risques métiers :** Les organisations dont le réseau est utilisé comme proxy peuvent être identifiées à tort comme sources d'attaques, entraînant des risques juridiques, opérationnels et de réputation.

**Vulnérabilités :**
L'article ne mentionne pas de CVE spécifique, car il s'agit d'une **exploitation fonctionnelle de composants légitimes** (SDK de proxy) intégrés de manière trompeuse ou non consensuelle dans des applications. Le vecteur d'attaque est la confiance accordée à des logiciels tiers et l'absence de contrôle sur le trafic sortant des appareils IoT/Smart TV.

**Recommandations :**
*   **Audit réseau :** Surveiller les requêtes DNS et le trafic sortant vers des domaines de services proxy connus (ex: `gmslb.net`, `ninjatech.io`, et autres domaines liés aux SDK de proxy).
*   **Contrôle d'accès :** Interdire l'utilisation d'appareils de streaming non approuvés ou de "boîtiers TV" inconnus sur les réseaux d'entreprise.
*   **Politique de sécurité :** Mettre en place une segmentation réseau stricte pour les appareils IoT/Smart TV afin d'isoler leur trafic des ressources critiques.
*   **Sensibilisation :** Informer les utilisateurs sur les risques de confidentialité liés à l'installation d'applications gratuites ("gratuiciels") sur les téléviseurs connectés et autres appareils domestiques.
*   **Régulation :** Les entreprises doivent exiger des plateformes (LG, Samsung) des contrôles plus stricts sur les SDK autorisés dans leurs magasins d'applications, à l'instar des politiques restrictives adoptées par Roku ou Amazon.

---
[Source](https://krebsonsecurity.com/2026/06/popa-botnet-linked-to-publicly-traded-israeli-firm/){:target="_blank"}
