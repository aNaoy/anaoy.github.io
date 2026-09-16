---
title: 'Attacker Hijacks AI Coding Assistant Session, Spreads Shai-Hulud Across About 100 Repositories'
date: 2026-09-16
permalink: /posts/2026/09/16/attacker-hijacks-ai-coding-assistant-session-spreads-shai-hulud-across-about-100-repositories/
tags:
- veille-cyber
- hackernews
---
### Compromission de la chaîne d'approvisionnement via un assistant de codage IA

Une attaque sophistiquée a permis à un pirate de détourner une session active d'un assistant de codage IA chez un fournisseur SaaS, entraînant la propagation du ver "Shai-Hulud" au sein d'une centaine de dépôts de code internes. L'attaquant a exploité la confiance accordée aux recommandations de l'IA pour injecter du code malveillant et exfiltrer des identifiants sensibles.

**Points clés :**
* **Détournement de session :** Le pirate a pris le contrôle d'une session d'assistant IA active, utilisant cette légitimité pour proposer des dépendances logicielles empoisonnées.
* **Propagation virale :** Une fois le code malveillant accepté, un infostealer a été installé, permettant le vol de jetons OAuth GitHub et la diffusion automatique du ver dans 100 dépôts.
* **Contamination par namespace :** Le pirate a empoisonné un paquet officiel de l'entreprise, provoquant une infection secondaire lorsqu'un autre employé a récupéré cette version compromise.
* **Évolution de la menace :** Les attaquants délaissent l'utilisation de l'IA pour la simple productivité au profit de son intégration directe dans des malwares et des opérations actives.

**Vulnérabilités :**
* Aucune CVE spécifique n'est mentionnée, car l'attaque repose sur une exploitation logique : le manque de vérification des recommandations générées par l'IA et l'accès excessif des extensions aux secrets (clés API, jetons OAuth).

**Recommandations :**
* **Validation rigoureuse :** Vérifier systématiquement les dépendances tierces recommandées par l'IA via des sommes de contrôle cryptographiques et des listes d'autorisation strictes.
* **Isolation des secrets :** Ne pas stocker de clés API brutes ou de jetons OAuth à longue durée de vie dans des emplacements accessibles par les extensions d'assistance.
* **Contrôle des flux :** Centraliser et filtrer tout le trafic lié aux dépendances via des dépôts internes contrôlés pour éviter l'installation de paquets malveillants provenant de sources publiques non vérifiées.

---
[Source](https://thehackernews.com/2026/09/attacker-hijacks-ai-coding-assistant.html){:target="_blank"}
