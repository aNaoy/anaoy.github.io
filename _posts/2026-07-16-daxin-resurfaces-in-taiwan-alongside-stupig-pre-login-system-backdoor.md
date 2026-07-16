---
title: 'Daxin Resurfaces in Taiwan Alongside Stupig Pre-Login SYSTEM Backdoor'
date: 2026-07-16
permalink: /posts/2026/07/16/daxin-resurfaces-in-taiwan-alongside-stupig-pre-login-system-backdoor/
tags:
- veille-cyber
- hackernews
---
### Résurgence de Daxin et découverte du backdoor Stupig : une menace persistante

Une cyberattaque sophistiquée, liée à des acteurs chinois, a été détectée en 2026 au sein d'une entreprise manufacturière à Taïwan. Elle implique le retour du rootkit **Daxin** et la découverte d'un nouveau backdoor nommé **Stupig**. Ces outils, dont les composants datent de 2013, suggèrent une intrusion potentiellement active depuis plus de 13 ans.

**Points clés :**
*   **Stupig :** Un backdoor agissant comme un fournisseur de disposition de clavier (DLL). Chargé par `winlogon.exe`, il permet l'exécution de commandes avec les privilèges **SYSTEM** directement depuis l'écran de connexion Windows, sans authentification préalable.
*   **Daxin :** Un rootkit en mode noyau qui intercepte le trafic TCP légitime pour ses communications C2 (Command & Control), rendant sa détection réseau extrêmement difficile. Il permet le mouvement latéral même dans des segments isolés du réseau.
*   **Tactique avancée :** L'utilisation de Stupig permet aux attaquants d'obtenir un accès total avant même l'ouverture de session utilisateur, évitant ainsi les journaux d'audit de connexion classiques.
*   **Modernisation des attaques :** Parallèlement, des acteurs affiliés à la Chine ont été observés utilisant des modèles d'IA (Claude Code et DeepSeek) pour automatiser l'ingénierie des attaques, la création de scripts et le contournement de défenses.

**Vulnérabilités exploitées :**
*   L'infection initiale proviendrait probablement d'un portail SSO (Digiwin) obsolète utilisant des versions du **JDK (1.5/1.6)** arrivées en fin de vie (EOL) depuis 2011.

**Recommandations :**
*   **Mise à jour logicielle :** Éliminer impérativement les composants logiciels obsolètes et non supportés (JDK anciens, portails SSO non mis à jour).
*   **Surveillance des DLL :** Auditer les modules chargés par `winlogon.exe` et surveiller l'enregistrement de nouveaux fournisseurs de disposition de clavier.
*   **Analyse du trafic :** Mettre en œuvre une analyse comportementale avancée pour détecter les anomalies dans les flux TCP, le rootkit Daxin ne créant pas de connexions sortantes distinctes mais détournant des connexions légitimes.
*   **Renforcement du périmètre :** Étant donné l'utilisation de l'IA pour générer des campagnes de phishing et automatiser l'exploitation, renforcer la vigilance sur les accès distants et les mécanismes d'authentification.

---
[Source](https://thehackernews.com/2026/07/daxin-resurfaces-in-taiwan-alongside.html){:target="_blank"}
