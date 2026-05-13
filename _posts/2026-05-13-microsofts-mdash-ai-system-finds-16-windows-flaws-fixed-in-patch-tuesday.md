---
title: 'Microsofts MDASH AI System Finds 16 Windows Flaws Fixed in Patch Tuesday'
date: 2026-05-13
permalink: /posts/2026/05/13/microsofts-mdash-ai-system-finds-16-windows-flaws-fixed-in-patch-tuesday/
tags:
- veille-cyber
- hackernews
---
### MDASH : L'IA au service de la découverte proactive de vulnérabilités Windows

Microsoft a introduit **MDASH** (*multi-model agentic scanning harness*), un système d'IA multi-agents conçu pour automatiser la détection, la validation et la preuve de vulnérabilités dans des bases de code complexes. Contrairement aux approches par modèle unique, MDASH orchestre plus de 100 agents spécialisés travaillant en concert (auditeurs, débatteurs et prouveurs) pour confirmer l'exploitabilité des failles identifiées.

**Points clés :**
* **Fonctionnement par étapes :** Analyse de la surface d'attaque, audit par des agents spécialisés, validation par débat entre modèles et preuve finale.
* **Fiabilité :** Le système utilise le désaccord entre agents comme indicateur de crédibilité pour filtrer les faux positifs.
* **Performance :** Cette solution a permis d'identifier 16 vulnérabilités corrigées lors du récent *Patch Tuesday*, notamment dans les couches réseau et d'authentification de Windows.

**Vulnérabilités majeures identifiées :**
* **CVE-2026-33824 (Score CVSS : 9.8) :** Vulnérabilité de type *double-free* dans `ikeext.dll`. Permet à un attaquant non authentifié d'exécuter du code à distance (RCE) via des paquets contrefaits envoyés à une cible utilisant IKEv2.
* **CVE-2026-33827 (Score CVSS : 8.1) :** Condition de concurrence (*race condition*) dans le pilote `tcpip.sys`. Permet une exécution de code à distance (RCE) via l'envoi de paquets IPv6 spécifiques sur des systèmes activant IPSec.

**Recommandations :**
* **Application immédiate des correctifs :** Il est impératif d'installer les dernières mises à jour de sécurité de Microsoft afin de corriger les failles identifiées lors du *Patch Tuesday*.
* **Veille sécuritaire :** Les organisations doivent surveiller activement les bulletins de sécurité MSRC (Microsoft Security Response Center) pour protéger leurs infrastructures contre les vecteurs d'attaque de type RCE sur les protocoles réseau (IKEv2, IPv6/IPSec).

---
[Source](https://thehackernews.com/2026/05/microsofts-mdash-ai-system-finds-16.html){:target="_blank"}
