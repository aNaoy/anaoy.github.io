---
title: 'Eclipse Foundation Mandates Pre-Publish Security Checks for Open VSX Extensions'
date: 2026-02-05
permalink: /posts/2026/02/05/eclipse-foundation-mandates-pre-publish-security-checks-for-open-vsx-extensions/
tags:
- veille-cyber
- hackernews
---
**Renforcement de la sécurité pour les extensions Open VSX**

La fondation Eclipse mettra en place des vérifications de sécurité avant la publication des extensions pour son registre Open VSX. Jusqu'à présent, la détection des extensions malveillantes se faisait principalement après leur publication. Ce nouveau système vise à adopter une approche proactive pour contrer les menaces liées à la chaîne d'approvisionnement logicielle, qui ciblent de plus en plus les développeurs via des places de marché d'extensions.

**Points clés :**

*   **Changement de stratégie :** Passage d'une approche réactive (suppression après signalement) à une approche proactive (vérification avant publication).
*   **Motivation :** Augmentation du volume de publications et évolution des menaces, rendant l'approche réactive insuffisante.
*   **Contexte :** Les registres d'extensions open source sont devenus des cibles d'attaques (usurpation de nom, typosquatting, propagation de mises à jour compromises).
*   **Mécanisme :** Les extensions suspectes seront mises en quarantaine pour examen au lieu d'être publiées immédiatement.
*   **Déploiement :** Le mois de février 2026 servira de période de surveillance sans blocage pour ajuster le système. L'application stricte débutera le mois suivant.

**Vulnérabilités ciblées (scénarios identifiés pour la mise en quarantaine) :**

*   Usurpation évidente de nom d'extension ou d'espace de noms.
*   Publication accidentelle de credentials ou de secrets.
*   Présence de schémas malveillants connus.
*   *(Aucun CVE spécifique n'est mentionné dans l'article pour ces types de menaces dans le contexte d'Open VSX.)*

**Recommandations :**

*   Mise en œuvre de vérifications de sécurité automatiques avant la publication des extensions.
*   Mise en quarantaine des extensions potentiellement dangereuses pour un examen manuel.
*   Adaptation d'un processus similaire à celui de Microsoft pour le Visual Studio Marketplace.
*   L'objectif est d'élever le niveau de sécurité général, d'aider les éditeurs à identifier les problèmes en amont et d'améliorer la confiance dans l'infrastructure Open VSX.

---
[Source](https://thehackernews.com/2026/02/eclipse-foundation-mandates-pre-publish.html){:target="_blank"}
