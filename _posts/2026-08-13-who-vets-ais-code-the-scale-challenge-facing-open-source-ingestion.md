---
title: 'Who Vets AI’s Code? The Scale Challenge Facing Open Source Ingestion'
date: 2026-08-13
permalink: /posts/2026/08/13/who-vets-ais-code-the-scale-challenge-facing-open-source-ingestion/
tags:
- veille-cyber
- bleepingcomp
---
### La menace du « Slopsquatting » : sécuriser l'ingestion de code IA

L'adoption massive des outils d'IA générative pour le développement logiciel crée un décalage critique entre la vitesse de production de code et les capacités actuelles de revue de sécurité. Ce phénomène expose les entreprises à des risques accrus au niveau de leur chaîne d'approvisionnement logicielle.

**Points clés :**
*   **Hallucinations de dépendances :** Les modèles LLM recommandent fréquemment des bibliothèques logicielles qui n'existent pas dans les registres publics (PyPI, npm).
*   **Exploitation malveillante :** Les attaquants surveillent ces suggestions pour enregistrer des noms de paquets fictifs (« slopsquatting ») et y injecter du code malveillant, qui est ensuite automatiquement intégré dans les environnements de build via les agents IA.
*   **Pression sur l'Open Source :** La prolifération de code généré par IA, souvent de moindre qualité ou contenant des défauts cachés (+70% de défauts constatés), surcharge les mainteneurs de projets communautaires.
*   **Obsolescence des contrôles :** Les outils d'analyse de composition logicielle (SCA) post-commit sont inefficaces face à la vitesse de génération, générant un volume d'alertes trop important pour être traité manuellement.

**Vulnérabilités :**
*   **Slopsquatting (Exploitation par hallucination de paquets) :** Bien que ce vecteur soit une pratique émergente plutôt qu'une CVE unique répertoriée, il s'apparente aux attaques de type *typosquatting*. L'article souligne que près de 50 % des dépendances suggérées par les IA qui existent réellement contiennent des CVE connues ou sont obsolètes.

**Recommandations :**
*   **Restreindre les accès aux registres :** Empêcher les postes de travail et les agents IA d'interroger directement les dépôts publics non vérifiés.
*   **Isolation des dépendances :** Placer tout nouveau paquet suggéré dans un environnement isolé (sandbox) pour analyse avant son intégration dans les branches principales.
*   **Gouvernance à l'ingestion :** Mettre en place un catalogue curaté et pré-validé de composants logiciels. L'idée est de passer d'une approche réactive (scanner après coup) à une approche proactive, en s'assurant que chaque bibliothèque provient d'une source de confiance avant même que le développeur ne l'intègre au build.

---
[Source](https://www.bleepingcomputer.com/news/security/who-vets-ais-code-the-scale-challenge-facing-open-source-ingestion/){:target="_blank"}
