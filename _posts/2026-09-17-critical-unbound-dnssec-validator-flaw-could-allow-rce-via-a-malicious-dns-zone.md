---
title: 'Critical Unbound DNSSEC Validator Flaw Could Allow RCE via a Malicious DNS Zone'
date: 2026-09-17
permalink: /posts/2026/09/17/critical-unbound-dnssec-validator-flaw-could-allow-rce-via-a-malicious-dns-zone/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans le résolveur DNS Unbound

Le résolveur DNS Unbound, dans toutes les versions jusqu’à la 1.26.0 incluse, présente plusieurs vulnérabilités de sécurité majeures, dont deux failles critiques pouvant mener à l'exécution de code à distance (RCE).

**Points clés :**
*   **Vecteur d'attaque :** Les vulnérabilités peuvent être exploitées via des zones DNS malveillantes envoyant des réponses contrefaites à un résolveur vulnérable.
*   **Impact :** Les risques principaux incluent le déni de service (DoS) et l'exécution de code arbitraire avec des privilèges système.
*   **Historique :** Aucune exploitation active n'a été signalée pour le moment. Un total de neuf correctifs est inclus dans la version 1.26.1.

**Vulnérabilités majeures :**
*   **CVE-2026-81642 (Critique) :** Débordement de tampon (heap overflow) dans le validateur DNSSEC lors du traitement des enregistrements DNSKEY.
*   **CVE-2026-82717 (Élevée) :** Corruption de mémoire (heap corruption) lors de la synthèse de CNAME, pouvant mener à une RCE selon les options de compilation.
*   **Autres CVE :** Sept autres vulnérabilités de sévérité moyenne à faible (CVE-2026-81634, CVE-2026-77955, CVE-2026-78227, CVE-2026-80225, CVE-2026-82720, CVE-2026-85501, CVE-2026-77860) impactant principalement la disponibilité et causant des dénis de service.

**Recommandations :**
*   **Mise à jour :** Installer immédiatement la version **Unbound 1.26.1**, qui corrige l'ensemble de ces vulnérabilités.
*   **Correctifs manuels :** Si une mise à jour complète n'est pas possible, NLnet Labs met à disposition des correctifs (patchs) spécifiques applicables sur le code source de la version 1.26.0.
*   **Configuration :** Notez qu'avec le correctif pour CVE-2026-85501, l'option `val-clean-additional` est désormais désactivée par défaut, modifiant le comportement de validation DNSSEC des sections additionnelles.

---
[Source](https://thehackernews.com/2026/09/critical-unbound-dnssec-validator-flaw.html){:target="_blank"}
