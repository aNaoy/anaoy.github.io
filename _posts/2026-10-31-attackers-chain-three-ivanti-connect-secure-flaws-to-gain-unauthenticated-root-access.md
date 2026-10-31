---
title: 'Attackers Chain Three Ivanti Connect Secure Flaws to Gain Unauthenticated Root Access'
date: 2026-10-31
permalink: /posts/2026/10/31/attackers-chain-three-ivanti-connect-secure-flaws-to-gain-unauthenticated-root-access/
tags:
- veille-cyber
- hackernews
---
### Chaînage d'exploits critiques dans Ivanti Connect Secure

Des attaquants, identifiés sous le nom de groupe UTA0576, exploitent activement une chaîne de trois vulnérabilités dans les produits Ivanti Connect Secure (ICS) pour obtenir un accès root non authentifié. Contrairement aux méthodes habituelles de déploiement de web shells, les attaquants utilisent cet accès pour l'exfiltration de données (identifiants, métadonnées Active Directory), la reconnaissance réseau et le vol de clés de récupération BitLocker.

**Vulnérabilités exploitées :**

*   **CVE-2026-104935** (Score CVSS : 8.6) : Contournement de l'authentification.
*   **CVE-2026-111357** (Score CVSS : 8.8) : Élévation de privilèges locale (LPE) due à une absence d'authentification sur une fonction critique.
*   **CVE-2026-118527** (Score CVSS : 4.3) : Génération de nombres prévisibles permettant l'upload de fichiers arbitraires.

**Points clés :**
*   L'enchaînement de ces failles permet une exécution de code à distance avec des privilèges root sans aucune authentification préalable.
*   La CISA a ajouté ces vulnérabilités à son catalogue *Known Exploited Vulnerabilities* (KEV) en raison de leur exploitation active.
*   Ivanti a confirmé que les correctifs sont désormais disponibles après une phase initiale de déploiement partiel.

**Recommandations :**
*   **Mise à jour immédiate :** Appliquer les correctifs fournis par Ivanti en mettant à jour vers les versions **25.1.1.3** ou **22.8R2.6** (ou versions ultérieures).
*   **Conformité :** Les agences fédérales américaines doivent appliquer les correctifs pour CVE-2026-111357 avant le 2 novembre 2026 et pour CVE-2026-118527 avant le 13 novembre 2026.
*   **Surveillance :** Inspecter les logs pour détecter toute activité suspecte liée à une exfiltration de données ou une reconnaissance de l'infrastructure Active Directory.

---
[Source](https://thehackernews.com/2026/10/attackers-chain-three-ivanti-connect.html){:target="_blank"}
