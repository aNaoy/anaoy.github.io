---
title: 'Viral Moltbot AI assistant raises concerns over data security'
date: 2026-01-29
permalink: /posts/2026/01/29/viral-moltbot-ai-assistant-raises-concerns-over-data-security/
tags:
- veille-cyber
- bleepingcomp
---
## Vulnérabilités et risques liés à l'assistant IA Moltbot

Des chercheurs en sécurité alertent sur les déploiements d'assistants IA open-source, tels que Moltbot (anciennement Clawdbot), dans les environnements d'entreprise. Ces configurations peuvent entraîner des fuites de données sensibles, notamment des clés API, des jetons OAuth, l'historique des conversations et des identifiants.

Moltbot permet une intégration profonde avec le système et les applications de l'utilisateur, fonctionnant localement 24h/24 et 7j/7 avec une mémoire persistante. Sa facilité d'installation a contribué à sa popularité rapide.

Cependant, une utilisation négligente expose à plusieurs risques :

**Points Clés et Vulnérabilités :**

*   **Interfaces d'administration exposées :** Des centaines d'interfaces d'administration sont découvertes en ligne en raison de mauvaises configurations de proxys inverses. Cela permet souvent un accès non authentifié, le vol d'identifiants, l'accès à l'historique des conversations et même l'exécution de commandes système à un niveau root.
*   **Absence de sandboxing par défaut :** L'agent IA dispose par défaut des mêmes accès complets aux données que l'utilisateur, ce qui augmente considérablement la surface d'attaque.
*   **Exposition de jetons API et OAuth :** Des jetons sensibles peuvent être exposés dans les configurations.
*   **Stockage d'identifiants en clair :** Des identifiants peuvent être stockés sous le répertoire `~/.clawdbot/`.
*   **Fuite de données d'entreprise :** L'accès médiatisé par l'IA peut entraîner la divulgation d'informations confidentielles de l'entreprise.
*   **Attaques par injection de prompt étendues :** La conception de l'agent peut être vulnérable à des attaques visant à manipuler ses réponses.
*   **Attaques par la chaîne d'approvisionnement :** Des "Skills" (modules) malveillantes peuvent être distribuées via le registre officiel, comme démontré par une attaque via un "ping" payload qui a été artificiellement promu.
*   **Imitation par des extensions malveillantes :** Des extensions malveillantes, comme une fausse extension VSCode, peuvent se faire passer pour Moltbot et installer des logiciels malveillants (ex: ScreenConnect RAT).
*   **Ciblage par des logiciels malveillants d'extraction d'informations :** Des malwares tels que RedLine, Lumma et Vidar sont susceptibles d'être adaptés pour cibler le stockage local de Moltbot afin de voler des données sensibles et des identifiants.

**Vulnérabilités spécifiques mentionnées (sans CVE) :**

*   Mauvaise configuration de proxys inverses exposant les interfaces d'administration.
*   Approbation automatique des connexions "locales" traitant le trafic internet comme fiable.
*   Absence de sandboxing par défaut pour l'agent IA.
*   Possibilité de stockage d'identifiants en clair.

**Recommandations :**

*   **Isolation dans une machine virtuelle :** Pour un déploiement sécurisé, il est crucial d'isoler l'instance de l'IA dans une machine virtuelle.
*   **Configuration du pare-feu :** Mettre en place des règles de pare-feu pour contrôler strictement l'accès à internet de l'instance IA.
*   **Éviter l'exécution directe sur le système hôte avec des privilèges root :** Ne pas exécuter Moltbot directement sur le système d'exploitation avec des droits d'administrateur.
*   **Vigilance accrue pour les entreprises :** Les entreprises doivent être conscientes que des employés peuvent utiliser Moltbot sans approbation IT, créant ainsi des risques significatifs.
*   **Surveillance des vulnérabilités :** Restez informé des avertissements de sécurité émis par diverses organisations spécialisées.

---
[Source](https://www.bleepingcomputer.com/news/security/viral-moltbot-ai-assistant-raises-concerns-over-data-security/){:target="_blank"}
