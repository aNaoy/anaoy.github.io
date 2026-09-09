---
title: 'The EU CRAs Real Question: What Shipped, and When Did You Know?'
date: 2026-09-09
permalink: /posts/2026/09/09/the-eu-cras-real-question-what-shipped-and-when-did-you-know/
tags:
- veille-cyber
- bleepingcomp
---
### L'impact du Cyber Resilience Act (CRA) sur la gestion des vulnérabilités

L'entrée en vigueur prochaine du *Cyber Resilience Act* (CRA) de l'Union européenne impose aux fabricants de logiciels des obligations strictes en matière de transparence et de réactivité. À partir du 11 septembre 2026, les entreprises devront notifier l'ENISA dans les 24 heures suivant la découverte d'une exploitation active d'une vulnérabilité, avec un rapport complet sous 72 heures. Cette exigence transforme la gestion des logiciels open source, omniprésents (98 % des applications), en un défi opérationnel et juridique majeur.

**Points clés :**
*   **Contrainte de temps :** Le délai de 72 heures pour rapporter une vulnérabilité est bien inférieur au délai moyen actuel de remédiation industrielle (environ 55 jours).
*   **Transparence des SBOM (Software Bill of Materials) :** L'article 13 du CRA exige des inventaires logiciels actualisés en permanence. Les SBOM générés statiquement et ponctuellement ne suffisent plus.
*   **Évolution des menaces :** Les responsables de projets doivent se préparer à des extorsions ou des divulgations massives de vulnérabilités, réelles ou gonflées, qui forcent les équipes à une réactivité immédiate.
*   **Responsabilité accrue :** Le passage d'une gestion volontaire à une obligation légale signifie que les entreprises doivent prouver la provenance et l'intégrité de chaque composant intégré.

**Vulnérabilités :**
*   L'article ne cite pas de CVE spécifique, mais illustre le risque via le phénomène des rapports de vulnérabilités « gonflés » (souvent utilisés pour l'extorsion) et souligne l'exposition liée à l'utilisation de composants open source non vérifiés.

**Recommandations :**
*   **Automatisation de la chaîne de production :** Instrumenter les pipelines de développement pour générer automatiquement des SBOM mis à jour à chaque modification.
*   **Gestion proactive de la provenance :** Adopter des catalogues de composants pré-vérifiés et attestés afin de garantir la sécurité avant même l'intégration dans le code.
*   **Test de préparation :** Effectuer des exercices de simulation : identifier un produit sorti il y a six mois et mesurer le temps nécessaire pour générer son SBOM et vérifier l'historique des CVE critiques le concernant. Si ce délai dépasse 72 heures, le processus interne doit être révisé.

---
[Source](https://www.bleepingcomputer.com/news/security/the-eu-cras-real-question-what-shipped-and-when-did-you-know/){:target="_blank"}
