---
title: '545 Hackers Tested It First. Now XRanges for AI Scores Your Security Agent'
date: 2026-09-23
permalink: /posts/2026/09/23/545-hackers-tested-it-first-now-xranges-for-ai-scores-your-security-agent/
tags:
- veille-cyber
- hackernews
---
### Évaluation et standardisation des agents de sécurité autonomes avec XRanges for AI

Les agents de sécurité autonomes sont capables de générer des rapports de vulnérabilités, mais il est difficile de vérifier la véracité de leurs découvertes, leur rigueur d'exploration ou leur respect des règles d'engagement. XRanges for AI, développé par CTF.ae, propose une solution pour mesurer objectivement la performance de ces agents grâce à une instrumentation en temps réel.

**Points clés :**
*   **Infrastructure de test réaliste :** La plateforme déploie des applications complexes et multi-services contenant des vulnérabilités injectées (dont des *zero-days* non publics) pour simuler des environnements réels.
*   **Instrumentation interne :** Contrairement à une analyse externe, l'outil utilise l'instrumentation (OpenTelemetry) intégrée au cœur des services pour observer précisément les actions de l'agent.
*   **Approche expérimentale :** La plateforme permet de tester plusieurs modèles et configurations de manière parallèle, avec une gestion intégrée des résultats via API.
*   **Validation par les faits :** Chaque action est corrélée aux traces système, éliminant les faux positifs et détectant les bugs inventés ou les chemins non explorés.

**Les quatre indicateurs de performance (signaux) :**
1.  **Couverture :** Mesure l'exhaustivité de l'exploration des fonctionnalités métier (ce que l'agent a visité vs ce qu'il a ignoré).
2.  **Limites (Boundaries) :** Vérifie le respect des règles d'engagement (ex: interdiction de supprimer des données ou de révoquer des clés API).
3.  **Exploitation :** Suivi étape par étape des chaînes d'exploitation (kill chains) pour confirmer si une vulnérabilité a été réellement compromise.
4.  **Intégrité :** Surveille la santé de l'environnement cible pour s'assurer que l'agent n'a pas cassé le système en tentant d'exploiter une faille.

**Vulnérabilités :**
*   L'article ne liste pas de CVE spécifiques, car il se concentre sur une **méthodologie d'évaluation**. Cependant, la plateforme utilise des vulnérabilités injectées sur mesure dans des environnements isolés, incluant des *zero-days* exclusifs pour tester la capacité de détection des agents.

**Recommandations pour les équipes de développement :**
*   **Passer de la lecture de rapports à l'analyse de télémétrie :** Ne vous fiez pas au texte généré par l'IA, mais aux données OpenTelemetry pour vérifier l'activité réelle.
*   **Privilégier la reproductibilité :** Utilisez des déploiements isolés pour comparer les variantes de prompts et de modèles sur des cibles identiques afin d'isoler la variance de la performance réelle.
*   **Automatiser les tests :** Intégrez l'évaluation dans les pipelines CI via l'API de la plateforme pour garantir une évaluation continue à chaque évolution de l'agent.
*   **Respecter les règles d'engagement :** Surveillez proactivement les violations de limites pendant les tests pour éviter que l'agent ne cause des dommages collatéraux inutiles.

---
[Source](https://thehackernews.com/2026/09/545-hackers-tested-it-first-now-xranges.html){:target="_blank"}
