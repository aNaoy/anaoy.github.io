---
title: 'JPCERT Confirms Active Command Injection Attacks on Array AG Gateways'
date: 2025-12-05
permalink: /posts/2025/12/05/jpcert-confirms-active-command-injection-attacks-on-array-ag-gateways/
tags:
- veille-cyber
- hackernews
---
### Exploitation de vulnérabilités sur les passerelles Array AG

Des attaques par injection de commandes sont activement menées contre les passerelles Array AG Series depuis août 2025, comme le confirme JPCERT/CC. Cette vulnérabilité, qui ne dispose pas d'identifiant CVE, concerne la fonctionnalité DesktopDirect, utilisée pour l'accès à distance aux postes de travail.

L'exploitation de cette faille permettrait aux attaquants d'exécuter des commandes arbitraires sur les systèmes affectés. JPCERT/CC a constaté des incidents au Japon où des web shells ont été déployés sur des appareils vulnérables, les attaques semblant provenir de l'adresse IP 194.233.100[.]138. Les détails sur l'ampleur des attaques et l'identité des acteurs malveillants ne sont pas encore connus.

Bien qu'une vulnérabilité d'évasion d'authentification (CVE-2023-28461) ait été exploitée l'année précédente par le groupe MirrorFace, aucune preuve ne lie actuellement cet acteur aux nouvelles attaques.

**Points clés :**

*   **Produit affecté :** Passerelles Array AG Series, spécifiquement la fonctionnalité DesktopDirect.
*   **Type d'attaque :** Injection de commandes.
*   **Impact :** Exécution de commandes arbitraires à distance.
*   **Activité observée :** Déploiement de web shells sur les systèmes compromis.
*   **Origine des attaques constatées :** Adresse IP 194.233.100[.]138.

**Vulnérabilités :**

*   **Type :** Injection de commandes (sans identifiant CVE).
*   **Versions affectées :** ArrayOS versions 9.4.5.8 et antérieures.

**Recommandations :**

*   Appliquer la mise à jour ArrayOS version 9.4.5.9 dès que possible.
*   Si la mise à jour n'est pas immédiate, désactiver les services DesktopDirect.
*   Utiliser le filtrage d'URL pour bloquer l'accès aux URL contenant un point-virgule.

---
[Source](https://thehackernews.com/2025/12/jpcert-confirms-active-command.html){:target="_blank"}
