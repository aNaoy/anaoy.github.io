---
title: 'US warns of AI-powered attacks on Siemens PLCs in critical infrastructure'
date: 2026-08-19
permalink: /posts/2026/08/19/us-warns-of-ai-powered-attacks-on-siemens-plcs-in-critical-infrastructure/
tags:
- veille-cyber
- bleepingcomp
---
### Menace croissante sur les automates Siemens dans les infrastructures critiques

Les agences fédérales américaines (CISA, NSA, FBI, etc.) alertent sur une campagne active visant les automates programmables industriels (API) Siemens de la gamme S7. Les attaquants utilisent l'intelligence artificielle pour générer des scripts d'exploitation personnalisés, facilitant l'accès aux systèmes de contrôle industriel.

**Points clés :**
* **Cibles :** Automates Siemens S7-200, S7-300, S7-400, S7-1200 et S7-1500.
* **Secteurs visés :** Énergie, eau, agroalimentaire, chimie, fabrication critique et base industrielle de défense.
* **Mode opératoire :** Utilisation d'outils de scan (Censys, ZoomEye) pour identifier les API exposés sur Internet. L'exploitation repose sur des scripts Python utilisant la bibliothèque `snap7` pour interagir avec le protocole S7comm, permettant de lire/écrire dans la mémoire des automates et de modifier leur configuration.
* **Objectifs :** Reconnaissance persistante, vol de données, sabotage d'équipements et interruption des services essentiels.

**Vulnérabilités :**
L'exploitation tire profit de la combinaison d'appareils exposés sur Internet, d'authentifications faibles, de logiciels obsolètes et de vulnérabilités critiques non corrigées dans les API. (Note : L'article ne mentionne pas de CVE spécifiques, mais souligne l'exploitation de failles de sécurité connues sur des systèmes non mis à jour).

**Recommandations :**
* **Inventaire :** Réaliser un recensement complet des automates Siemens S7 présents dans le réseau.
* **Isolation :** Bloquer l'accès direct des automates à Internet.
* **Maintenance :** Installer systématiquement les dernières mises à jour de sécurité fournies par Siemens.
* **Renforcement :** Appliquer des contrôles d'accès stricts pour limiter les privilèges.
* **Surveillance :** Mettre en place un monitoring des activités réseau pour détecter tout comportement anormal ciblant les dispositifs OT.

---
[Source](https://www.bleepingcomputer.com/news/security/us-warns-of-ai-powered-attacks-on-siemens-plcs-in-critical-infrastructure/){:target="_blank"}
