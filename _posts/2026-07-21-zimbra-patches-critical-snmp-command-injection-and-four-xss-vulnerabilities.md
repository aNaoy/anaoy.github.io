---
title: 'Zimbra Patches Critical SNMP Command Injection and Four XSS Vulnerabilities'
date: 2026-07-21
permalink: /posts/2026/07/21/zimbra-patches-critical-snmp-command-injection-and-four-xss-vulnerabilities/
tags:
- veille-cyber
- hackernews
---
### Correctifs de sécurité critiques pour Zimbra 10.1.20

Zimbra a déployé la version 10.1.20 pour corriger neuf vulnérabilités majeures au sein de sa suite collaborative. Bien qu'aucune exploitation active ne soit signalée à ce jour, la sévérité des failles découvertes impose une mise à jour rapide des environnements exposés.

**Points clés :**
*   **Injection de commandes :** Une vulnérabilité critique affecte le composant de surveillance SNMP lorsque les notifications sont activées.
*   **Faille de contournement :** Un défaut permet aux utilisateurs authentifiés de contourner les restrictions de transfert d'e-mails, facilitant potentiellement l'exfiltration de données (CVE-2026-50055).
*   **Risques XSS :** Quatre failles de type Cross-Site Scripting (XSS) dans le « Classic Web Client » ont été colmatées. Celles-ci pouvaient être exploitées via des noms de fichiers de pièces jointes malveillants ou des champs de saisie spécialement conçus pour exécuter des scripts lors du rendu.

**Vulnérabilités identifiées :**
*   **CVE-2026-50055 :** Contournement des restrictions de transfert d'e-mails.
*   **Injection de commandes SNMP :** Risque lié aux notifications SNMP.
*   **Quatre vulnérabilités XSS :** Affectant le traitement des pièces jointes et des champs de formulaire dans le client web classique.

**Recommandations :**
*   **Mise à jour immédiate :** Installer sans délai la version **Zimbra 10.1.20** pour bénéficier des correctifs.
*   **Veille sécuritaire :** Compte tenu de l'historique d'exploitation des failles XSS dans cette suite, appliquer une politique de gestion des correctifs rigoureuse pour minimiser la surface d'attaque.

---
[Source](https://thehackernews.com/2026/07/zimbra-patches-critical-snmp-command.html){:target="_blank"}
