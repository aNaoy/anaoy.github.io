---
title: 'Android Adds Intrusion Logging for Sophisticated Spyware Forensics'
date: 2026-05-13
permalink: /posts/2026/05/13/android-adds-intrusion-logging-for-sophisticated-spyware-forensics/
tags:
- veille-cyber
- hackernews
---
### Android renforce la lutte contre les logiciels espions avec l'Intrusion Logging

Google a introduit l'**Intrusion Logging**, une nouvelle fonctionnalité intégrée au mode « Protection avancée » d'Android. Conçue pour les utilisateurs à haut risque, elle permet de collecter des preuves forensiques afin d'analyser des attaques sophistiquées par des logiciels espions.

**Points clés :**
* **Journalisation persistante :** Enregistrement quotidien des activités système (processus applicatifs, connexions réseau, transferts USB, changements de certificats, verrouillage).
* **Sécurité des données :** Les journaux sont chiffrés de bout en bout et stockés sur les serveurs de Google. Seul l'utilisateur possède les clés, garantissant que ni Google ni des acteurs étatiques ne peuvent y accéder.
* **Résilience :** Les données, conservées 12 mois, sont inaccessibles, indélébiles et immodifiables, même par un malware ayant infecté l'appareil.
* **Usage :** Les journaux peuvent être téléchargés par l'utilisateur pour être soumis à des experts en cybersécurité pour une analyse forensique.

**Vulnérabilités adressées :**
L'article ne mentionne pas de CVE spécifiques, mais cible les menaces liées aux outils de surveillance avancés (spywares), au vol d'identifiants via des trojans bancaires, au spoofing d'appels financiers, et aux attaques exploitant les protocoles obsolètes (2G).

**Recommandations :**
* **Activation :** Activer le mode « Protection avancée » via les paramètres de sécurité (nécessite Android 16 ou version ultérieure).
* **Gestion des données :** Une fois les journaux téléchargés et déchiffrés, l'utilisateur devient seul responsable de leur sécurité physique et logique.
* **Précautions d'usage :** Garder à l'esprit que les journaux réseau enregistrent également les connexions DNS en mode navigation privée (Chrome).
* **Mise à jour :** Maintenir le système à jour pour bénéficier des nouvelles mesures de protection (détection de menaces en temps réel, chiffrement post-quantique, et blocage des API d'accessibilité abusives).

---
[Source](https://thehackernews.com/2026/05/android-adds-intrusion-logging-for.html){:target="_blank"}
