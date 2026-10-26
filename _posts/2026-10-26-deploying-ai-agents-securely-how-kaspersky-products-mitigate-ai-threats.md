---
title: 'Deploying AI agents securely: how Kaspersky products mitigate AI threats'
date: 2026-10-26
permalink: /posts/2026/10/26/deploying-ai-agents-securely-how-kaspersky-products-mitigate-ai-threats/
tags:
- veille-cyber
- securelist
---
### Sécurisation des agents IA en entreprise : Stratégies de défense

L'intégration croissante des agents d'IA dans les infrastructures d'entreprise expose les organisations à de nouveaux vecteurs d'attaque. Ces outils, s'ils ne sont pas supervisés, peuvent être détournés pour accéder à des données sensibles ou exécuter des commandes malveillantes.

**Points clés :**
*   **Risques émergents :** Les agents d'IA (ex: Claude, LM Studio, ChatGPT) peuvent être utilisés par des attaquants pour automatiser des tâches malveillantes (création de logiciels malveillants, exécution de scripts) ou être exploités via des attaques de type "ClickFix".
*   **Expansion des menaces :** Plus de 2 500 vulnérabilités liées aux outils et modèles d'IA (LLM) ont été publiées entre 2025 et 2026.
*   **Approche de défense :** La protection repose sur une visibilité accrue, le contrôle des applications, la surveillance comportementale EDR et l'analyse du contenu (skills et modèles).

**Vulnérabilités :**
Bien que l'article ne liste pas de CVE spécifiques, il souligne une recrudescence massive de vulnérabilités dans les versions logicielles des outils IA et leurs plugins. Les vecteurs critiques identifiés sont :
*   L'injection de code dans des « skills » (instructions externes).
*   La présence de code malveillant au sein des fichiers de modèles (formats .pth, .pt, .pkl, .kers).
*   L'utilisation d'agents en mode "auto-approval" (YOLO mode) ou sans bac à sable (sandbox).

**Recommandations :**
*   **Contrôle granulaire :** Utiliser des outils d'administration (Application Control) pour limiter l'exécution d'agents IA aux seuls besoins professionnels, via une stratégie de liste blanche ou de liste noire.
*   **Filtrage Web :** Bloquer l'accès aux services « IA as a Service » non approuvés via les outils de contrôle du Web.
*   **Surveillance comportementale (EDR) :** Déployer des règles spécifiques pour détecter :
    *   L'accès inhabituel aux fichiers sensibles par des agents.
    *   L'exécution d'agents dans des configurations risquées (YOLO mode).
    *   La création d'artefacts suspects liés aux serveurs MCP (Model Context Protocol).
*   **Analyse de contenu :** Scanner systématiquement les « skills » téléchargés et les fichiers de modèles LLM avant leur déploiement afin d'identifier des charges utiles malveillantes via des moteurs d'analyse spécialisés.
*   **Veille proactive :** Utiliser des portails de Threat Intelligence pour cartographier les tactiques et techniques (MITRE ATT&CK) associées aux agents d'IA utilisés par les groupes cybercriminels.

---
[Source](https://securelist.com/tr/how-to-secure-ai-agents/121444/){:target="_blank"}
