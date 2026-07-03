---
title: 'NetNut proxy network disrupted, 2 million infected devices cut off'
date: 2026-07-03
permalink: /posts/2026/07/03/netnut-proxy-network-disrupted-2-million-infected-devices-cut-off/
tags:
- veille-cyber
- bleepingcomp
---
### Démantèlement du réseau de proxys résidentiels NetNut

Une opération internationale coordonnée par Google, le FBI et plusieurs partenaires de cybersécurité a permis de neutraliser NetNut (également connu sous le nom de Popa), un vaste réseau de proxys résidentiels détournant environ 2 millions d'appareils Android, notamment des téléviseurs connectés et des boîtiers de streaming.

**Points clés :**
*   **Fonctionnement :** Le réseau utilisait des logiciels malveillants, dont des variantes du botnet « Badbox 2.0 », pour transformer les appareils infectés en nœuds de sortie. Cela permettait aux cybercriminels de masquer leur trafic malveillant derrière des adresses IP résidentielles légitimes.
*   **Utilisation malveillante :** Plus de 300 groupes de menace, incluant des acteurs de cybercriminalité et d'espionnage, exploitaient ce réseau pour mener des attaques par pulvérisation de mots de passe (password-spraying) et accéder aux infrastructures des victimes.
*   **Interconnexion :** NetNut agissait comme un pilier majeur de l'industrie des proxys, vendant ses services en marque blanche à d'autres réseaux, ce qui signifie que son démantèlement impacte tout l'écosystème des proxys résidentiels.

**Vulnérabilités :**
*   **Infections par chaîne d'approvisionnement :** Certains appareils sont infectés par des logiciels préinstallés lors de la fabrication.
*   **Applications trojanisées :** L'installation d'applications malveillantes via des sources non vérifiées permet l'intégration des appareils dans le botnet via des plugins de proxy.
*   *Note : Aucune CVE spécifique n'est mentionnée, car l'attaque repose sur l'exploitation de logiciels malveillants et l'intégration de kits de développement (SDK) malveillants plutôt que sur une faille logicielle unique.*

**Recommandations :**
*   **Utilisation de Google Play Protect :** Maintenir cette fonctionnalité active sur les appareils Android pour détecter et désactiver automatiquement les applications malveillantes.
*   **Vigilance sur les applications :** Éviter de télécharger des applications provenant de sources tierces ou non fiables qui pourraient contenir des plugins de proxy malveillants.
*   **Surveillance réseau :** Les administrateurs réseau doivent surveiller les comportements inhabituels des appareils IoT et multimédias, qui sont souvent utilisés comme points d'entrée par les botnets en raison de leur sécurité généralement plus faible.

---
[Source](https://www.bleepingcomputer.com/news/security/netnut-proxy-network-disrupted-2-million-infected-devices-cut-off/){:target="_blank"}
