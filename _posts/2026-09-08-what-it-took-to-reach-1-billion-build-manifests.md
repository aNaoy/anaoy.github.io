---
title: 'What It Took to Reach 1 Billion Build Manifests'
date: 2026-09-08
permalink: /posts/2026/09/08/what-it-took-to-reach-1-billion-build-manifests/
tags:
- veille-cyber
- hackernews
---
### L'automatisation par l'IA pour sécuriser la supply chain logicielle à grande échelle

Chainguard a atteint le cap symbolique du milliard de manifestes de construction (build manifests) pour ses images conteneurisées, marquant une évolution majeure dans la gestion de la sécurité logicielle. Face à l'automatisation croissante des attaques, l'entreprise a dû repenser son infrastructure de production pour passer d'un système réactif à un modèle auto-correcteur.

**Points clés :**
*   **Volumétrie :** Plus de 1 milliard de manifestes produits, couvrant 3 000+ images uniques et 675 000 versions.
*   **Infrastructure "Factory 2.0" :** Transition d'un système événementiel (générateur de goulots d'étranglement et d'erreurs) vers un système de réconciliation continue nommé **DriftlessAF**.
*   **Rôle de l'IA :** Les agents IA gèrent les tâches complexes de tri, les backports de correctifs et la prise de décision, libérant les ingénieurs des tâches répétitives et réduisant le "temps de cycle" de défense face aux vulnérabilités.
*   **Modèle de sécurité :** Chaque artefact est généré avec une provenance SLSA Level 3, des signatures Sigstore et une nomenclature logicielle (SBOM) complète.

**Vulnérabilités :**
*   L'article ne mentionne pas de CVE spécifique, mais souligne la menace systémique du "CVE doom loop" (boucle infernale de gestion des vulnérabilités) : le retard accumulé entre la découverte d'une faille dans l'amont et le déploiement d'une image corrigée. La solution mise en place vise à réduire ce délai à quasi zéro.

**Recommandations :**
*   **Adopter une approche déclarative :** Passer de processus manuels ou événementiels à un état désiré défini, permettant au système de converger automatiquement vers la sécurité.
*   **Automatiser la réconciliation :** Utiliser des systèmes qui comparent en continu l'état actuel avec l'état souhaité pour corriger automatiquement les dérives (drift).
*   **Intégration de l'IA ciblée :** Réserver l'IA aux arbitrages complexes et à la gestion des dépendances tout en conservant des processus de construction déterministes et vérifiables pour garantir l'intégrité du code.
*   **Transparence de la supply chain :** Prioriser la génération systématique de SBOM et de preuves de provenance (SLSA) pour assurer une traçabilité totale des composants.

---
[Source](https://thehackernews.com/2026/09/what-it-took-to-reach-1-billion-build.html){:target="_blank"}
