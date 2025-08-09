---
title: 'Researchers Uncover GPT-5 Jailbreak and Zero-Click AI Agent Attacks Exposing Cloud and IoT Systems'
date: 2025-08-09
permalink: /posts/2025/08/09/researchers-uncover-gpt-5-jailbreak-and-zero-click-ai-agent-attacks-exposing-cloud-and-iot-systems/
tags:
- veille-cyber
- hackernews
---
**Avancées et Risques des Agents IA : Contournement des Garde-fous et Exploitation Zero-Click**

Des chercheurs ont développé une technique de "jailbreak" nommée "Echo Chamber", combinée à une approche narrative, pour contourner les protections éthiques de modèles de langage comme GPT-5. Cette méthode permet de susciter des réponses indésirables en introduisant subtilement des contextes compromis, transformant des requêtes potentiellement illicites en élucubrations déguisées en continuité narrative. La méthode a déjà été utilisée pour contourner les défenses de xAI Grok 4.

Parallèlement, des attaques dites "zero-click" exploitent l'intégration des modèles d'IA avec des services externes. La suite d'attaques "AgentFlayer" utilise des vulnérabilités dans les connecteurs ChatGPT (par exemple, Google Drive) pour exfiltrer des données sensibles via des invites cachées dans des documents apparemment inoffensifs. D'autres attaques exploitent des tickets Jira malveillants pour dérober des secrets via l'éditeur de code IA Cursor, ou ciblent Microsoft Copilot Studio à l'aide d'e-mails spécialement conçus. Ces failles, liées à des principes similaires à "EchoLeak", exploitent l'autonomie des agents IA pour des manipulations discrètes sans interaction utilisateur directe.

L'augmentation de l'utilisation des agents IA dans des contextes critiques, couplée à leur connexion à des systèmes externes, élargit considérablement la surface d'attaque potentielle, introduisant des vulnérabilités ou des données non fiables de manière exponentielle. Ces découvertes soulignent l'insuffisance des filtres basés uniquement sur les mots-clés ou l'intention dans des contextes conversationnels complexes et l'importance de la sécurité conçue et non présumée.

**Points Clés :**

*   **Jailbreak "Echo Chamber" :** Technique permettant de contourner les garde-fous des LLM en utilisant des contextes conversationnels subtilement compromis et une narration pour masquer les intentions malveillantes.
*   **Vulnérabilités Zero-Click :** Exploitations qui ne nécessitent aucune action de l'utilisateur pour exfiltrer des données ou manipuler des systèmes via des agents IA connectés à des services externes.
*   **Exemples d'Attaques Zero-Click :**
    *   "AgentFlayer" : Exploitation des connecteurs ChatGPT (Google Drive) via des invites dissimulées.
    *   Utilisation de tickets Jira malveillants avec l'éditeur de code IA Cursor.
    *   Ciblage de Microsoft Copilot Studio via des e-mails piégés.
*   **Risques Accrus :** L'intégration des IA avec des systèmes externes augmente la surface d'attaque et les risques d'introduction de données non fiables.
*   **Limitations des Défenses Actuelles :** Les filtres basés sur les mots-clés ou l'intention sont insuffisants dans des scénarios multi-tours où le contexte peut être progressivement corrompu.

**Vulnérabilités Mentionnées :**

*   Technique de jailbreak "Echo Chamber" (sans CVE spécifique identifiée dans l'article pour cette technique elle-même).
*   Attaques "AgentFlayer" (décrites comme une sous-catégorie des primitives "EchoLeak", sans CVE spécifique attribuée à "AgentFlayer" ou "EchoLeak" dans l'article).
*   Exploitation des connecteurs ChatGPT (ex: Google Drive).
*   Vulnérabilités dans l'intégration de l'éditeur de code IA Cursor avec des systèmes comme Jira.
*   Vulnérabilités dans Microsoft Copilot Studio.

**Recommandations Implicites / Mentionnées :**

*   Mise en œuvre de contre-mesures comme un filtrage de sortie strict.
*   Réalisation de "red teaming" réguliers pour identifier les failles.
*   Nécessité de développer des sécurités pour les agents IA et de ne pas les considérer comme acquises.
*   Développement d'une approche équilibrée entre la confiance dans les systèmes d'IA et leur sécurité.
*   Les protections disponibles contre ces manipulations devraient être déployées (mentionné par Zenity Labs).

---
[Source](https://thehackernews.com/2025/08/researchers-uncover-gpt-5-jailbreak-and.html){:target="_blank"}
