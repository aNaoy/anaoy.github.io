---
title: 'DShield Honeypot Update, (Mon, May 4th)'
date: 2026-05-04
permalink: /posts/2026/05/04/dshield-honeypot-update-mon-may-4th/
tags:
- veille-cyber
- sans-isc
---
### Mise à jour des honeypots DShield : Compatibilité et maintenance

Le SANS Internet Storm Center déploie des mises à jour pour ses honeypots DShield, visant à assurer la compatibilité avec les systèmes d'exploitation récents et à améliorer les capacités de capture.

**Points clés :**
*   **Compatibilité OS :** Prise en charge optimisée pour Ubuntu 26.04 et 24.04 LTS. Fin du support pour les versions 20.04 et 22.04.
*   **Raspberry Pi :** Amélioration du support pour les versions "trixie" et "bookworm" (32 et 64 bits).
*   **Cowrie :** Mise à jour du honeypot SSH/Telnet Cowrie pour intégrer de nouvelles fonctionnalités.
*   **Authentification :** Les anciennes clés API (encodées en base64) deviennent obsolètes et doivent être remplacées par les nouvelles clés (chaînes hexadécimales) pour permettre la remontée des logs.

**Vulnérabilités :**
*   Aucune CVE spécifique n'est mentionnée dans cet article ; les changements sont d'ordre fonctionnel et liés à la gestion des dépendances logicielles (notamment Rust et Python).

**Recommandations :**
*   **Réinstallation propre :** Lors d'un passage à une version majeure de l'OS, il est fortement conseillé de réinstaller le honeypot à partir de zéro plutôt que d'effectuer une mise à jour sur place (conserver uniquement le fichier `dshield.ini`).
*   **Mise à jour des accès :** Si les logs Cowrie ne remontent plus, générez et configurez une nouvelle clé d'authentification sur votre compte DShield.
*   **Automatisation :** Maintenir les mises à jour automatiques activées pour bénéficier des correctifs de sécurité et des ajustements de compatibilité.

---
[Source](https://isc.sans.edu/diary/rss/32948){:target="_blank"}
