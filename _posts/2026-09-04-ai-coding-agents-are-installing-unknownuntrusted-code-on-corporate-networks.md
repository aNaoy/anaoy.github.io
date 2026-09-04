---
title: 'AI Coding Agents Are Installing Unknown/Untrusted Code on Corporate Networks'
date: 2026-09-04
permalink: /posts/2026/09/04/ai-coding-agents-are-installing-unknownuntrusted-code-on-corporate-networks/
tags:
- veille-cyber
- schneier
---
### Risques d'injection de code via les agents IA de développement

Les agents d'IA générative utilisés pour le développement logiciel présentent une faille de sécurité majeure : ils accordent une confiance aveugle aux fichiers `llms.txt` et `llms-full.txt` présents sur les sites web, sans vérifier l'authenticité des ressources externes qu'ils recommandent. Des chercheurs ont démontré qu'en enregistrant des domaines ou des paquets obsolètes cités dans ces fichiers, il est possible de pousser les agents à exécuter du code arbitraire au sein des réseaux d'entreprises (notamment Fortune 500).

**Points clés :**
* **Vulnérabilité contextuelle :** Les agents traitent la documentation technique comme une vérité absolue et automatique, ce qui permet des attaques par empoisonnement de la chaîne d'approvisionnement.
* **Exécution automatique :** Une fois le code malveillant installé, l'agent déclenche une communication vers un serveur distant (beaconing), exposant les données internes.
* **Multiplicité des agents :** Des outils comme Claude, Codex et Hermes ont été identifiés comme vecteurs d'installation de ce code non approuvé.

**Vulnérabilités :**
* Aucune CVE spécifique n'est associée à cette faille, car il s'agit d'un problème systémique de **logique de confiance (Trust Model)** plutôt que d'un bug de code unique. La vulnérabilité réside dans le processus décisionnel des agents IA.

**Recommandations :**
* **Vigilance humaine :** Ne jamais permettre à un agent d'IA d'exécuter du code ou d'installer des dépendances sans une revue humaine approfondie des sources.
* **Audit des dépendances :** Mettre en place des outils de scan et de vérification des paquets tiers avant toute intégration dans le workflow de développement.
* **Isolation :** Exécuter les agents d'IA dans des environnements isolés (sandboxes) avec des accès réseau restreints pour limiter le risque de "phone-home" (connexion sortante vers des serveurs malveillants).

---
[Source](https://www.schneier.com/blog/archives/2026/09/ai-coding-agents-are-installing-unknown-untrusted-code-on-corporate-networks.html){:target="_blank"}
