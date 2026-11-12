---
title: 'ThreatsDay: 59 Linux Kernel Bugs, Falcon Spyware, GSocket Backdoors + 17 More Stories'
date: 2026-11-12
permalink: /posts/2026/11/12/threatsday-59-linux-kernel-bugs-falcon-spyware-gsocket-backdoors-17-more-stories/
tags:
- veille-cyber
- hackernews
---
### Panorama des Menaces Cyber : Analyse de la semaine

L'actualité de la cybersécurité souligne une industrialisation des attaques, facilitée par l'intelligence artificielle (IA) tant pour le développement de malwares que pour la manipulation des résultats de recherche. Les attaquants exploitent désormais la confiance accordée aux outils légitimes et aux identités d'entreprise.

#### Points clés
*   **Blanchiment de cryptomonnaies :** Le réseau lié au piratage de Binance (6,43 milliards $) utilise des méthodes automatisées complexes, incluant la création de "meme coins" pour dissimuler l'origine des fonds.
*   **Persistance via GSocket :** Une augmentation de 356 % des détections de cet outil open-source montre que les attaquants l'utilisent pour maintenir un accès aux serveurs Linux même après le patch des vulnérabilités initiales.
*   **Espionnage browser-based :** Le framework Falcon (variant de PeckBirdy) compromet les navigateurs via JavaScript pour exfiltrer des cookies de session, mots de passe et emails, visant des institutions gouvernementales.
*   **Infrastructures IA ciblées :** Les plateformes d'orchestration comme Flowise sont de plus en plus visées pour détourner les agents IA et générer des playbooks d'exploitation automatisés.
*   **Phishing de nouvelle génération :** Le "BluePhishing" abuse du consentement OAuth pour créer des identités d'agents malveillants dans des environnements cloud, évitant ainsi les alertes de phishing traditionnelles.

#### Vulnérabilités notables
*   **Linux Kernel (CVE-2026-64563) :** Une faille de type "state-reset" dans la bibliothèque *rhashtable* permettant une élévation de privilèges locale sur Linux et Android.
*   **RPC Runtime (CVE-2026-118737) :** Faille critique (score CVSS 8.1) permettant l'exécution de code à distance.
*   **Flowise (CVE-2025-59528 et CVE-2026-41264) :** Vulnérabilités exploitées pour compromettre des systèmes d'IA.

#### Recommandations stratégiques
*   **Défense en profondeur :** Le patching logiciel est nécessaire mais insuffisant. Il est impératif de rechercher activement des signes de persistance (outils de contrôle à distance comme GSocket, connexions sortantes suspectes).
*   **Gouvernance des accès :**
    *   Renforcer la surveillance des comptes de prestataires externes, vecteurs fréquents d'intrusion pour les rançongiciels comme *Citrus*.
    *   Auditer strictement les permissions OAuth accordées aux applications et aux agents IA (éviter les consentements "one-time" non vérifiés).
*   **Hygiène sécuritaire :**
    *   Mettre en œuvre le chiffrement NTLM imposé par les mises à jour Windows pour contrer les attaques par relais.
    *   Surveiller les dépôts de code (GitHub) pour éviter l'exposition accidentelle de secrets API (ex: cas du *Planning Inspectorate*).
*   **Vérification de la chaîne d'approvisionnement :** Utiliser les nouveaux signaux de provenance et onglets de sécurité sur les plateformes comme PyPI pour vérifier l'intégrité des paquets installés.

---
[Source](https://thehackernews.com/2026/11/threatsday-59-linux-kernel-bugs-falcon.html){:target="_blank"}
