---
title: 'Help TDS Linked to Hotejka as 20,000+ Cloudflare Pages Domains Host Tech Support Scams'
date: 2026-10-15
permalink: /posts/2026/10/15/help-tds-linked-to-hotejka-as-20000-cloudflare-pages-domains-host-tech-support-scams/
tags:
- veille-cyber
- hackernews
---
### Hotejka et « Help TDS » : une menace persistante d'escroqueries au support technique

Le système de distribution de trafic (TDS) nommé **Help TDS** est une infrastructure cybercriminelle active depuis 2017, liée au programme d'affiliation russophone **Hotejka** (considéré comme une évolution de l'opération ROI777). Ce réseau détourne le trafic de sites web compromis, principalement WordPress, pour rediriger les internautes vers des arnaques au support technique.

**Points clés :**
*   **Mode opératoire :** Les attaquants injectent des plugins malveillants ou des scripts HTML dans des sites WordPress pour capturer les visiteurs.
*   **Infrastructure :** Help TDS utilise la plateforme de tracking Keitaro et génère massivement des domaines via **Cloudflare Pages** (plus de 20 000 domaines détectés depuis avril 2026).
*   **Objectif :** Afficher de fausses alertes de sécurité Windows pour inciter les victimes à appeler un centre d'appels frauduleux, où des opérateurs utilisent l'ingénierie sociale pour obtenir un accès à distance (via des outils comme Ultraviewer) et installer des logiciels malveillants.
*   **Écosystème :** Le réseau collabore avec une vingtaine d'affiliés cybercriminels notoires, tels que *Balada Injector*, *Detour Dog* et *DollyWay*.

**Vulnérabilités exploitées :**
*   **Injections WordPress :** Utilisation de plugins malveillants (ex: `woocommerce_inputs`) ou de blocs HTML injectés directement dans les sites CMS.
*   **Exploitation des ressources légitimes :** Abus massif de plateformes d'hébergement cloud (Cloudflare Pages) et de services de tracking publicitaires (Keitaro) pour masquer les redirections malveillantes.
*   *Note : Aucune CVE spécifique n'est mentionnée, car l'attaque repose principalement sur l'injection de code et l'exploitation de sites web mal sécurisés ou vulnérables aux compromissions d'administration.*

**Recommandations :**
*   **Sécurisation WordPress :** Maintenir les plugins et le noyau WordPress à jour, supprimer les extensions inutilisées et auditer régulièrement les fichiers sources pour détecter des injections suspectes.
*   **Hygiène numérique :** Sensibiliser les utilisateurs à ignorer les alertes de sécurité s'affichant en plein écran dans un navigateur et à ne jamais autoriser de prise de contrôle à distance par un correspondant non sollicité.
*   **Filtrage réseau :** Surveiller les comportements de redirection inhabituels et bloquer le trafic provenant de sources de redirection connues comme malveillantes.
*   **Sécurité des accès :** Imposer une authentification forte (MFA) sur tous les accès d'administration de sites web pour limiter les risques de compromission initiale.

---
[Source](https://thehackernews.com/2026/10/help-tds-linked-to-hotejka-as-20000.html){:target="_blank"}
