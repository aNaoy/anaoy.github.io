---
title: 'Slopsquatting, Phantom Domains, and HalluSquatting Are the Same AI Attack'
date: 2026-07-24
permalink: /posts/2026/07/24/slopsquatting-phantom-domains-and-hallusquatting-are-the-same-ai-attack/
tags:
- veille-cyber
- bleepingcomp
---
### La faille du « Late Binding » : Menaces sur les agents de codage IA

Le développement récent de l'IA générative a révélé une vulnérabilité critique affectant les agents de codage (GitHub Copilot, Cursor, Windsurf, etc.) : la confiance aveugle accordée aux noms générés par hallucination. Les attaquants exploitent désormais la prédictibilité de ces modèles pour anticiper les noms de domaines, de paquets logiciels ou de dépôts que l'IA va « inventer », afin de les enregistrer et d'y injecter du code malveillant.

#### Points clés
*   **Mécanisme d'attaque :** L'agent IA génère un identifiant inexistant par hallucination. L'attaquant, ayant prédit cet identifiant, a déjà réservé la ressource correspondante. Lorsque l'agent tente d'exécuter la commande ou de récupérer la dépendance, il télécharge et exécute automatiquement le code malveillant de l'attaquant.
*   **Évolution des menaces :** Trois variantes ont été identifiées en six mois :
    *   **Slopsquatting (janvier 2026) :** Cible les paquets npm.
    *   **Phantom Squatting (juin 2026) :** Cible les domaines web.
    *   **HalluSquatting (juillet 2026) :** Cible les dépôts et les « skills » (outils) des agents, permettant un déploiement massif via les permissions étendues accordées aux agents.
*   **Inopérance des défenses classiques :** Les scanners de sécurité traditionnels et les certificats (SSL/DNSSEC) sont inefficaces, car ils valident l'identité de la ressource ou son contenu déclaré, mais pas l'intention ou l'intégrité réelle de la charge utile (« payload ») lors de l'exécution automatique.

#### Vulnérabilités
*   **Défaut de conception (Late Binding) :** Les pipelines d'automatisation exécutent du code provenant de sources externes sans vérification préalable (« vetting »), comblant le fossé entre la génération de texte par l'IA et l'exécution système.
*   **Complexité de la chaîne de dépendances :** Les outils de sécurité scannent rarement les dépendances transitives profondes, permettant à des composants compromis d'être introduits silencieusement dans le cycle de vie logiciel.

#### Recommandations
*   **Verrouillage des pipelines :** Désactiver l'exécution automatique par défaut des outils récupérés par les agents et forcer une étape de validation humaine ou automatisée.
*   **Utilisation de catalogues conservés (Curated Catalogs) :** Centraliser la résolution des dépendances via des dépôts privés où chaque composant est vérifié et validé avant d'être accessible par l'agent.
*   **Vérification pré-fetch :** S'assurer que tous les frameworks d'agents sont configurés pour vérifier l'origine et l'intégrité des ressources avant toute tentative de téléchargement ou d'exécution.

---
[Source](https://www.bleepingcomputer.com/news/security/slopsquatting-phantom-domains-and-hallusquatting-are-the-same-ai-attack/){:target="_blank"}
