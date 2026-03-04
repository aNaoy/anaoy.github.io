---
title: 'When an AI Assistant Becomes Part of the Hacker’s Attack Chain | Security Analysis of Doubao Phone'
date: 2026-03-04
permalink: /posts/2026/03/04/when-an-ai-assistant-becomes-part-of-the-hackers-attack-chain-security-analysis-of-doubao-phone/
tags:
- veille-cyber
- zerodaysfans
---
### Le Doubao Assistant : Un Agent IA au Cœur des Risques Mobiles

L'intégration d'assistants IA aux capacités d'action autonome sur smartphone, comme le Doubao Assistant, transforme l'interaction utilisateur mais introduit de nouveaux vecteurs d'attaque. Ces agents, capables de percevoir, raisonner et agir, peuvent être détournés pour voler des informations sensibles.

**Points Clés :**

*   **Architecture :** Le Doubao Assistant fonctionne sur le système d'exploitation Obric, avec des modules clés tels qu'ObricAiAgent (orchestration des tâches), ObricAutoAction (automatisation), AIKernel (inférence IA locale) et MemoryData (gestion de la mémoire).
*   **Fonctionnement :** L'agent utilise une boucle "percevoir → raisonner → agir", capturant l'écran, envoyant les données au cloud pour inférence, puis exécutant l'action.
*   **Sécurité :** Des mesures de sécurité sont en place, notamment l'authentification des composants super-apps, l'utilisation d'un TEE pour la communication cloud sécurisée et le traitement distinct des écrans sensibles (via des images locales).
*   **Vulnérabilités Identifiées :** Des risques subsistent malgré les protections, notamment liés à la potentielle manipulation de l'agent par des messages malveillants.

**Vulnérabilités :**

*   **Risque de TOCTOU (Time-of-Check to Time-of-Use) dans l'interface graphique :** Un décalage temporel entre la décision d'une action et son exécution peut entraîner des actions non intentionnelles si l'interface évolue. Actuellement, les protections sont axées sur la validation avant exécution, mais les opérations complexes pourraient créer des fenêtres d'attaque.
    *   **CVE :** Non spécifié dans l'article.
*   **Injection de Prompt (Prompt Injection) :** Le modèle IA peut mal interpréter du contenu affiché à l'écran (texte ou images) comme de nouvelles instructions, le conduisant à des actions indésirables. L'agent peut être amené à divulguer des informations personnelles ou à participer à des chaînes d'attaque.
    *   **CVE :** Non spécifié dans l'article.

**Recommandations :**

*   **Protection contre le TOCTOU :** Développer des mécanismes de validation plus robustes pour les opérations futures impliquant des délais plus longs ou des séquences d'actions complexes.
*   **Renforcement contre l'injection de prompt :** Améliorer le filtrage et les contraintes sémantiques pour le contenu des captures d'écran, et renforcer les défenses côté cloud pour identifier et neutraliser les tentatives d'injection.
*   **Contrôles d'accès et de confidentialité :** S'assurer que les autorisations accordées aux agents IA restent strictement nécessaires et que les données sensibles sont protégées contre toute exposition involontaire ou malveillante.
*   **Gestion des opérations sensibles :** Maintenir des politiques claires et strictes interdisant ou exigeant une validation utilisateur manuelle pour les actions à haut risque (paiements, vérifications d'identité).

---
[Source](https://www.darknavy.org/blog/security_analysis_of_doubao_phone/){:target="_blank"}
