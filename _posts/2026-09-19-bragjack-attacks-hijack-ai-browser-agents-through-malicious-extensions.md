---
title: 'BragJack attacks hijack AI browser agents through malicious extensions'
date: 2026-09-19
permalink: /posts/2026/09/19/bragjack-attacks-hijack-ai-browser-agents-through-malicious-extensions/
tags:
- veille-cyber
- bleepingcomp
---
### BragJack : Le détournement des agents IA dans les navigateurs

La technique « BragJack » permet à une extension de navigateur malveillante de prendre le contrôle des assistants IA intégrés aux navigateurs (Chrome, Edge, Opera, etc.) sans interaction utilisateur. En exploitant les capacités de modification du trafic réseau (`declarativeNetRequest`), l'attaquant détourne les requêtes légitimes pour injecter ses propres instructions (« Prompt Forcing »). L'IA, utilisant ses privilèges natifs, exécute alors des actions malveillantes (lecture de fichiers, accès à la caméra/micro, actions sur les sites web) comme si elles provenaient de l'utilisateur.

**Points clés :**
*   **Prompt Forcing :** Contrairement à une injection de prompt classique, l'attaquant force l'agent IA à exécuter une séquence complète d'instructions légitimes avec ses privilèges élevés.
*   **Cibles :** Google Gemini Live, Perplexity Comet, Microsoft Edge, Opera Neon et Claude pour Chrome.
*   **Mécanisme :** Utilisation de règles DNR (*declarativeNetRequest*) pour affaiblir les en-têtes de sécurité, rediriger des ressources JavaScript et communiquer directement avec les composants privilégiés de l'IA.

**Vulnérabilités identifiées :**
*   **CVE-2026-0628 (Google Chrome/Gemini) :** Interception de requêtes permettant l'exécution de code dans le contexte de l'IA.
*   **CVE-2026-55945 (Microsoft Edge) :** Race condition permettant de contourner la séparation des modes « Think » et « Do » de l'agent.

**Recommandations :**
*   **Mises à jour :** Maintenir systématiquement le navigateur et ses composants à jour pour bénéficier des correctifs de sécurité.
*   **Gestion des extensions :** Supprimer les extensions inutilisées ou suspectes.
*   **Vigilance sur les permissions :** Être extrêmement prudent lors de l'installation d'extensions demandant des accès larges (« lire et modifier toutes vos données sur tous les sites Web »).

---
[Source](https://www.bleepingcomputer.com/news/security/bragjack-attacks-hijack-ai-browser-agents-through-malicious-extensions/){:target="_blank"}
