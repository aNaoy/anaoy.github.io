---
title: 'New VOLTA Infostealer Uses Claude, Gemini, and Kimi AI to Rank Victims by Financial Value'
date: 2026-11-02
permalink: /posts/2026/11/02/new-volta-infostealer-uses-claude-gemini-and-kimi-ai-to-rank-victims-by-financial-value/
tags:
- veille-cyber
- hackernews
---
### VOLTA : Le malware qui utilise l'IA pour prioriser ses victimes

Le nouveau cheval de Troie bancaire (infostealer) pour Windows, baptisé **VOLTA (ou VOLTA-AUTODOXER)**, marque une évolution dans les méthodes d'exfiltration. Contrairement aux malwares classiques, il intègre une couche d'intelligence artificielle générative pour analyser et classer automatiquement les données volées, permettant aux attaquants de cibler les victimes les plus rentables sans effort manuel.

**Points clés :**
*   **Architecture multi-IA :** Le malware utilise OpenRouter pour interroger des modèles comme Claude (Anthropic), Kimi (Moonshot AI) et Gemini (Google). En cas de refus de réponse par un modèle (filtrage de sécurité), il bascule automatiquement vers le suivant.
*   **Analyse intelligente :** Le logiciel agit comme un "analyste de renseignement forensique". Il génère un dossier structuré incluant une estimation de la valeur financière de la victime et une évaluation de sa posture de cybersécurité (hygiène des mots de passe).
*   **Vol de données étendu :** Il collecte des identifiants (navigateurs, comptes OAuth, SSH, cloud), des sessions de messagerie/jeux (Telegram, Discord, Roblox, Steam), des moyens de paiement et effectue des captures d'écran.
*   **Enrichissement :** Le malware fouille les boîtes Gmail des victimes pour corréler leurs adresses physiques avec des reçus de plateformes de livraison (Uber Eats, Amazon, etc.).
*   **Distribution :** VOLTA semble être commercialisé sous forme de kit (builder), permettant à des opérateurs moins expérimentés d'exécuter des campagnes ciblées.

**Vulnérabilités exploitées :**
*   L'article ne mentionne pas de CVE spécifique, car il s'agit d'une menace basée sur l'abus de fonctionnalités légitimes et l'exploitation de données personnelles déjà présentes sur la machine.
*   **Risque lié au "LLMjacking" :** Le malware (ainsi que d'autres outils comme NIK C2) peut détourner des clés API OpenAI présentes dans les variables d'environnement de la victime, faisant payer la puissance de calcul de l'attaque par la victime elle-même.

**Recommandations :**
*   **Sécurisation des environnements de développement :** Ne jamais stocker de clés API (OpenAI, cloud, etc.) dans les variables d'environnement du système ou en clair sur le disque dur.
*   **Authentification forte :** Déployer systématiquement l'authentification multifacteur (MFA) sur tous les comptes critiques, particulièrement pour les jetons OAuth et les messageries.
*   **Surveillance réseau :** Détecter les flux sortants inhabituels vers des API de routage de modèles (ex: OpenRouter) ou des exfiltrations répétées vers Telegram depuis des postes de travail.
*   **Hygiène numérique :** Appliquer le principe du moindre privilège et limiter l'accès aux données sensibles sur les machines professionnelles pour réduire le "bundle" de données exploitables par l'IA des attaquants.

---
[Source](https://thehackernews.com/2026/11/new-volta-infostealer-uses-claude.html){:target="_blank"}
