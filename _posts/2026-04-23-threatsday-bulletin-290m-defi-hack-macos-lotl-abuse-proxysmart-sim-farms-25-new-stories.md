---
title: 'ThreatsDay Bulletin: $290M DeFi Hack, macOS LotL Abuse, ProxySmart SIM Farms +25 New Stories'
date: 2026-04-23
permalink: /posts/2026/04/23/threatsday-bulletin-290m-defi-hack-macos-lotl-abuse-proxysmart-sim-farms-25-new-stories/
tags:
- veille-cyber
- hackernews
---
### Panorama des menaces cyber : De la supply chain au DeFi

Cette semaine, le paysage de la menace est marqué par une recrudescence d'attaques exploitant des vulnérabilités connues, des compromissions de la chaîne d'approvisionnement et des tactiques de détournement d'outils légitimes.

**Faits marquants et vulnérabilités critiques :**

*   **Piratage DeFi (290M$) :** KelpDAO a été victime d'un vol massif dû à une compromission de l'infrastructure RPC de LayerZero, attribuée au groupe nord-coréen TraderTraitor.
*   **Vulnérabilités actives :**
    *   **MajorDoMo :** **CVE-2026-27175** (injection de commande) et **CVE-2026-27174** (RCE non authentifié).
    *   **Apache ActiveMQ :** Chaîne d'exploitation sans identifiants via **CVE-2026-34197** et **CVE-2024-32114**.
    *   **Autres :** **CVE-2025-22952** (Elestio Memos) et **CVE-2024-57046** (Routeurs NETGEAR).
*   **Chaîne d'approvisionnement (Supply Chain) :** Multiplication de paquets npm malveillants (ex: `ixpresso-core`, `@velora-dex/sdk`, `mgc`) utilisés pour installer des backdoors SSH, voler des identifiants ou déployer des RAT comme *XWorm* et *minirat*.
*   **Abus de fonctionnalités légitimes :**
    *   Utilisation du mécanisme `.NET AppDomainManager` pour une exécution furtive.
    *   Détournement des métadonnées Spotlight sur macOS pour stocker des charges utiles évasives.
    *   Extension "StealTok" (Chrome/Edge) utilisant la configuration distante pour contourner les contrôles de sécurité.
*   **IA et automatisation :** Montée des injections indirectes de prompts (IPI) visant les agents IA et persistance des fermes de SIM (ProxySmart) facilitant la fraude à grande échelle.

**Recommandations de sécurité :**

1.  **Gestion des correctifs :** Prioriser la remédiation des CVE actives, particulièrement celles permettant l'exécution de code à distance (RCE) sans authentification.
2.  **Sécurité logicielle :** Auditer systématiquement les dépendances tierces (npm/PyPI) et limiter les permissions accordées aux extensions de navigateur et applications tierces.
3.  **Renforcement des accès :** Adopter les *Passkeys* comme standard d'authentification pour remplacer les mots de passe vulnérables au phishing.
4.  **Zero Trust et filtrage :** Ne jamais faire confiance aux entrées (input) par défaut, qu'il s'agisse d'interactions humaines ou d'agents IA, et segmenter l'accès aux infrastructures critiques (RPC, serveurs de gestion).
5.  **Surveillance :** Renforcer la visibilité sur les protocoles natifs (SMB, RDP, scripts macOS) souvent détournés pour des mouvements latéraux.

---
[Source](https://thehackernews.com/2026/04/threatsday-bulletin-290m-defi-hack.html){:target="_blank"}
