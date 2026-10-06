---
title: 'Google Pauses OSS Product Bug Bounty Rewards After Surge in Invalid Automated Reports'
date: 2026-10-06
permalink: /posts/2026/10/06/google-pauses-oss-product-bug-bounty-rewards-after-surge-in-invalid-automated-reports/
tags:
- veille-cyber
- hackernews
---
### Suspension du programme de primes aux bogues pour les logiciels open source de Google

Google a suspendu temporairement, depuis le 1er octobre, le versement de primes pour les rapports de vulnérabilités « produits » (défauts de conception ou d'implémentation) au sein de ses projets open source. Cette décision fait suite à une augmentation massive de soumissions automatisées, dont la grande majorité s'est révélée non valide, potentiellement générées par des outils d'intelligence artificielle (IA).

**Points clés :**
*   **Périmètre :** La suspension concerne les projets open source (ex: Go, Angular, Protocol Buffers). Les signalements de compromissions de la chaîne d'approvisionnement et les autres problèmes de sécurité (comme les fuites d'identifiants) restent éligibles aux récompenses.
*   **Historique :** Le programme, lancé en 2022, avait déjà tenté de limiter les rapports de faible qualité en 2026 en exigeant des preuves de concept plus solides.
*   **Calendrier :** Google prévoit de réévaluer et de modifier cette partie du programme au cours du premier trimestre 2027.

**Vulnérabilités concernées :**
*   Il n'y a pas de CVE spécifique mentionnée, car la mesure est structurelle et non liée à une faille précise.
*   Les vulnérabilités concernées sont celles affectant la confidentialité ou l'intégrité des données utilisateur (ex: corruption mémoire, *path traversal*).

**Recommandations pour les chercheurs :**
*   **Canaux alternatifs :** Les chercheurs sont invités à diriger leurs rapports vers le *Cloud VRP* pour les projets liés au Cloud, ou vers le *Patch Rewards Program* (qui récompense la soumission de correctifs plutôt que le simple signalement).
*   **Qualité des rapports :** Pour les projets qui acceptent encore des signalements, il est impératif de vérifier et filtrer rigoureusement toute sortie générée par des LLM avant soumission, sous peine de voir les rapports rejetés sans crédit.
*   **Politiques spécifiques :** Consulter les politiques de sécurité individuelles des projets (ex: le projet Go demande explicitement aux chercheurs de ne pas envoyer de rapports LLM non vérifiés).

---
[Source](https://thehackernews.com/2026/10/google-pauses-oss-product-bug-bounty.html){:target="_blank"}
