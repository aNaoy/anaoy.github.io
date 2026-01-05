---
title: 'Risks of OOB Access via IP KVM Devices, (Mon, Jan 5th)'
date: 2026-01-05
permalink: /posts/2026/01/05/risks-of-oob-access-via-ip-kvm-devices-mon-jan-5th/
tags:
- veille-cyber
- sans-isc
---
**Vulnerabilités et Sécurité des Dispositifs KVM IP Abordables**

L'émergence de dispositifs KVM (Keyboard, Video, Mouse) IP à bas coût, tels que le NanoKVM, offre des fonctionnalités d'accès à distance similaires aux solutions d'entreprise traditionnelles (IPMI), mais à une fraction du prix. Cependant, cette démocratisation s'accompagne de risques de sécurité significatifs.

**Points Clés :**

*   **Accessibilité accrue :** Des appareils comme le PIKVM, basés sur Raspberry Pi, et plus récemment le NanoKVM de Sipeed, ont rendu l'accès KVM IP plus accessible pour les particuliers et les petites entreprises.
*   **Risques de confiance du fournisseur :** Des accusations de portes dérobées intentionnelles et de négligence face aux vulnérabilités ont été émises à l'encontre de certains fabricants, notamment Sipeed.
*   **Nature sensible des KVM IP :** Ces dispositifs ont un accès direct aux systèmes, pouvant intercepter des frappes et afficher l'écran, les rendant des cibles critiques.
*   **Vulnérabilités communes :** Des problèmes tels que les mises à jour de firmware non sécurisées sont fréquents sur les appareils grand public. Le NanoKVM télécharge des mises à jour depuis des serveurs en Chine et peut transmettre des informations sur le système, avec des découvertes d'un microphone non documenté signalées.

**Vulnérabilités (CVE non spécifiés dans l'article, mais la nature des risques est soulignée) :**

*   Absence de mises à jour de sécurité robustes.
*   Potentiel de portes dérobées intégrées.
*   Collecte de données système potentiellement sensible.
*   Absence de fonctionnalités de sécurité essentielles comme l'authentification multifacteur (MFA) par défaut.

**Recommandations :**

1.  **Ne pas exposer à Internet :** Utiliser des solutions VPN comme Tailscale ou d'autres VPN pour accéder aux KVM à distance, évitant ainsi une exposition directe sur Internet.
2.  **Authentification forte :** Mettre en place des mécanismes d'authentification robustes, y compris, si possible, l'authentification multifacteur (MFA).
3.  **Configuration TLS :** Utiliser TLS avec des certificats valides (internes ou publics) pour chiffrer la connexion et prévenir les attaques de type "Man-in-the-Middle" (MitM).
4.  **Journalisation centralisée :** Configurer des journaux d'accès complets et les centraliser sur un serveur syslog, avec des alertes configurées pour les événements de connexion.
5.  **Sécurité de la console :** Assurer une authentification et des mesures de verrouillage d'écran sur le système auquel le KVM est connecté.
6.  **Tests réguliers :** Vérifier périodiquement le bon fonctionnement des dispositifs KVM et mettre en place des alertes en cas de dysfonctionnement.

---
[Source](https://isc.sans.edu/diary/rss/32598){:target="_blank"}
