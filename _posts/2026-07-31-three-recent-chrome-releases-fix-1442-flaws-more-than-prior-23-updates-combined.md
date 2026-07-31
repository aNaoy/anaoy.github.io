---
title: 'Three Recent Chrome Releases Fix 1,442 Flaws, More Than Prior 23 Updates Combined'
date: 2026-07-31
permalink: /posts/2026/07/31/three-recent-chrome-releases-fix-1442-flaws-more-than-prior-23-updates-combined/
tags:
- veille-cyber
- hackernews
---
### Explosion des vulnérabilités Chrome : Google accélère ses correctifs face à l'IA

Face à une augmentation exponentielle des vulnérabilités — accentuée par l'utilisation de modèles de langage (LLM) dans la recherche de failles — Google a corrigé 1 442 failles dans ses trois dernières versions de Chrome (149, 150 et 151). Ce volume dépasse le total cumulé des 23 mises à jour précédentes, illustrant la pression croissante exercée sur les cycles de développement.

**Points clés :**
*   **Rythme soutenu :** Google passe à un cycle de publication bimensuel pour les versions majeures et envisage deux mises à jour de sécurité hebdomadaires.
*   **Automatisation :** L'entreprise automatise la génération des notes de version et des CVE pour accélérer la divulgation publique.
*   **Innovation technique :** Travail sur le "patching dynamique" permettant de mettre à jour les processus en arrière-plan sans nécessiter de redémarrage complet du navigateur.
*   **Stratégie de fond :** Migration vers des langages mémoire-sûrs (Rust) et remplacement du C++ pour les composants critiques afin d'éliminer des classes entières de vulnérabilités.

**Vulnérabilité notable :**
*   **CVE-2026-3545 :** Faille critique de type "sandbox escape" dans le composant de navigation (score CVSS 9.6). Cette vulnérabilité, présente depuis 13 ans et découverte grâce à l'IA (Gemini), permettait d'accéder aux fichiers locaux du système.

**Recommandations :**
*   **Mises à jour systématiques :** Maintenir Chrome à jour en permanence pour bénéficier des correctifs de sécurité critiques.
*   **Redémarrages proactifs :** Bien que Google travaille sur des solutions transparentes, il est essentiel de redémarrer régulièrement le navigateur pour finaliser l'application des correctifs de sécurité.
*   **Modernisation :** Adopter les versions les plus récentes de Chrome pour profiter des nouvelles couches de sécurité basées sur Rust et la réduction de la dette technique C++.

---
[Source](https://thehackernews.com/2026/07/three-recent-chrome-releases-fix-1442.html){:target="_blank"}
