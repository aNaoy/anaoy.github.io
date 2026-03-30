---
title: 'The State of Secrets Sprawl 2026: 9 Takeaways for CISOs'
date: 2026-03-30
permalink: /posts/2026/03/30/the-state-of-secrets-sprawl-2026-9-takeaways-for-cisos/
tags:
- veille-cyber
- hackernews
---
### L'état de la prolifération des secrets en 2026 : un défi critique pour les CISO

La prolifération des secrets (mots de passe, clés API, jetons) s'accélère à une vitesse sans précédent, portée par l'adoption massive de l'IA et l'augmentation des outils de développement. Le rapport GitGuardian 2026 souligne une crise de sécurité où la simple détection ne suffit plus.

**Points clés :**
*   **Croissance exponentielle :** Le nombre de secrets exposés a augmenté de 152 % depuis 2021, surpassant largement la croissance du nombre de développeurs.
*   **Impact de l'IA :** Les fuites liées aux services d'IA ont bondi de 81 % en un an. Les nouveaux outils d'orchestration et d'infrastructure LLM sont particulièrement vulnérables.
*   **Risque interne :** Les dépôts de code internes sont 6 fois plus susceptibles de contenir des secrets que les dépôts publics.
*   **Fuites hors code :** 28 % des fuites surviennent dans des outils de collaboration (Slack, Jira, Confluence), où les secrets sont souvent plus critiques.
*   **Persistance des menaces :** 64 % des secrets divulgués en 2022 sont encore valides aujourd'hui, prouvant l'inefficacité des processus de rotation et de révocation.
*   **Vulnérabilité des infrastructures :** Les serveurs GitLab auto-hébergés et les registres Docker exposent des secrets à un taux 3 à 4 fois supérieur à GitHub. Les serveurs MCP (Model Context Protocol) ont, dès leur première année, causé l'exposition de plus de 24 000 secrets.

**Vulnérabilités majeures :**
*   **Secrets codés en dur (Hardcoded secrets) :** Présents massivement dans les dépôts internes, les images Docker et les configurations d'agents IA.
*   **Compromission des points de terminaison :** Les machines de développement et les runners CI/CD (ex: attaques *Shai-Hulud 2* et *LiteLLM*) deviennent des cibles prioritaires pour la récolte automatisée de jetons d'accès.
*   *(Note : Aucune CVE spécifique n'est mentionnée dans le rapport, car le problème relève de la mauvaise gestion des secrets et non d'une faille logicielle isolée).*

**Recommandations :**
*   **Gouvernance des identités non-humaines (NHI) :** Passer d'une simple détection à un programme de gestion complète des cycles de vie des identités (service accounts, agents IA, CI/CD).
*   **Rotation automatisée :** Rendre la rotation et la révocation des secrets routinières et automatisées pour éviter la persistance des accès.
*   **Sécurisation étendue :** Étendre les outils de scan au-delà du code source pour inclure les outils de collaboration, les infrastructures de build et les conteneurs.
*   **Vaulting par défaut :** Adopter des coffres-forts de secrets comme standard de travail pour les développeurs afin d'éliminer le stockage en clair ou dans des fichiers de configuration.

---
[Source](https://thehackernews.com/2026/03/the-state-of-secrets-sprawl-2026-9.html){:target="_blank"}
