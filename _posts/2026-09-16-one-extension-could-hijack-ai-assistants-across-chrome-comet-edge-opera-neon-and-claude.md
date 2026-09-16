---
title: 'One Extension Could Hijack AI Assistants Across Chrome, Comet, Edge, Opera Neon and Claude'
date: 2026-09-16
permalink: /posts/2026/09/16/one-extension-could-hijack-ai-assistants-across-chrome-comet-edge-opera-neon-and-claude/
tags:
- veille-cyber
- hackernews
---
### Risque de détournement des assistants IA dans les navigateurs

Des chercheurs en sécurité ont démontré qu'une simple extension de navigateur peut compromettre les assistants IA intégrés de cinq produits basés sur Chromium : **Chrome (Gemini Live), Perplexity Comet, Microsoft Edge, Opera Neon et Claude in Chrome**. En utilisant des permissions courantes (modification de pages web et du trafic réseau), une extension malveillante peut injecter son propre code dans les pages de confiance pour piloter l'agent IA, lire des fichiers locaux, capturer des captures d'écran ou activer la caméra et le micro.

**Points clés :**
* **Vecteur d'attaque :** L'attaque repose sur l'installation préalable d'une extension malveillante par l'utilisateur.
* **Mécanisme :** L'extension usurpe le canal de communication entre le navigateur et le serveur de l'IA en manipulant la page web de confiance (ex: `gemini.google.com`).
* **Sévérité variable :** Perplexity Comet présente les risques les plus élevés (accès aux fichiers, historique, captures d'écran), tandis que Claude in Chrome est considéré comme moins critique car il s'agit d'une extension détournant une autre extension.

**Vulnérabilités identifiées :**
* **CVE-2026-0628 (Chrome) :** Score 8.8. Corrigé dans la version 143.0.7499.192.
* **CVE-2026-55945 (Edge) :** Score 4.2. Corrigé dans la version 150.0.4078.48.
* **Autres produits (Comet, Opera Neon, Claude) :** Aucune CVE attribuée, mais des vulnérabilités de conception ont été confirmées et récompensées par des programmes de *bug bounty*.

**Recommandations :**
* **Mises à jour :** Mettre impérativement à jour Chrome et Edge vers les versions correctives mentionnées ci-dessus.
* **Gestion des extensions :** Passer en revue les extensions installées et supprimer celles qui ne sont pas nécessaires ou dont la provenance est douteuse.
* **Veille logicielle :** Pour les produits sans correctif public mentionné (Comet, Opera, Claude), maintenir le logiciel à jour et rester vigilant face aux nouvelles versions.

---
[Source](https://thehackernews.com/2026/09/one-extension-could-hijack-ai.html){:target="_blank"}
