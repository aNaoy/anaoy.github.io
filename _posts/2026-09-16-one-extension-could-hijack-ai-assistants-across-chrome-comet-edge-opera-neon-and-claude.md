---
title: 'One Extension Could Hijack AI Assistants Across Chrome, Comet, Edge, Opera Neon and Claude'
date: 2026-09-16
permalink: /posts/2026/09/16/one-extension-could-hijack-ai-assistants-across-chrome-comet-edge-opera-neon-and-claude/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité des assistants IA intégrés aux navigateurs : Le risque des extensions malveillantes

Des chercheurs en cybersécurité ont démontré qu'une extension de navigateur malveillante peut détourner les assistants IA intégrés de cinq produits : Google Chrome (Gemini Live), Perplexity Comet, Microsoft Edge, Opera Neon et l'extension Claude for Chrome. En exploitant les permissions standards des extensions (modification de pages web et contrôle du trafic réseau), un attaquant peut injecter du code dans les pages web de confiance, usurpant ainsi l'identité de l'utilisateur pour commander l'IA.

**Points clés :**
*   **Fonctionnement :** L'attaque repose sur le contrôle d'une page web "de confiance" écoutée par l'agent IA. L'extension détourne cette page pour envoyer ses propres instructions à l'agent.
*   **Gravité variable :** Les capacités varient selon le produit, allant du simple contrôle de l'agent IA à l'accès aux fichiers locaux, à la caméra/micro, aux captures d'écran et à l'historique de navigation. 
*   **Risque réel :** Bien qu'il s'agisse de démonstrations techniques sans preuves d'attaques actives, le vecteur d'attaque nécessite l'installation préalable d'une extension malveillante par l'utilisateur.

**Vulnérabilités identifiées :**
*   **CVE-2026-0628 (Chrome) :** Score de 8,8/10. Corrigé dans la version 143.0.7499.192.
*   **CVE-2026-55945 (Edge) :** Score de 4,2/10. Corrigé dans la version 150.0.4078.48.
*   **Comet, Opera Neon et Claude :** Vulnérabilités identifiées par les chercheurs mais ne disposant pas de CVE officiels au moment du rapport.

**Recommandations :**
*   **Mises à jour :** Maintenir impérativement Chrome (v.143+) et Edge (v.150+) à jour.
*   **Gestion des extensions :** Passer en revue et supprimer toute extension non indispensable ou de source douteuse, car elles constituent le vecteur d'entrée principal.
*   **Vigilance :** Pour les utilisateurs de Comet, Opera Neon et Claude, privilégier les mises à jour logicielles automatiques dès que les éditeurs déploient des correctifs de sécurité.

---
[Source](https://thehackernews.com/2026/09/one-extension-could-hijack-ai.html){:target="_blank"}
