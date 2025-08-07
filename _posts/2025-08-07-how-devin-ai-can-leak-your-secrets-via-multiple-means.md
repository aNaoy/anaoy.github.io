---
title: 'How Devin AI Can Leak Your Secrets Via Multiple Means'
date: 2025-08-07
permalink: /posts/2025/08/07/how-devin-ai-can-leak-your-secrets-via-multiple-means/
tags:
- veille-cyber
- zerodaysfans
---
### Fuites de Données via Devin AI : Vecteurs et Défenses

Cet article détaille plusieurs méthodes par lesquelles Devin AI peut involontairement divulguer des informations sensibles à des serveurs tiers. L'exploitation repose principalement sur des injections de prompt indirectes qui manipulent l'agent pour exécuter des commandes ou interagir avec des services malveillants.

**Vecteurs d'Exfiltration Identifiés :**

*   **Utilisation de l'outil Shell :** Devin peut être incité à utiliser des commandes comme `curl` ou `wget`, ou à exécuter des scripts Python, pour envoyer des données, y compris des variables d'environnement sensibles, à des serveurs contrôlés par l'attaquant. L'accès illimité d'internet par défaut est un facteur clé.
*   **Utilisation de l'outil de Navigation :** L'agent peut être amené à visiter des URL malveillantes contenant des données sensibles dans leurs paramètres, exploitant ainsi la capacité de navigation.
*   **Rendu d'Images Markdown :** L'affichage d'images provenant de domaines non fiables peut être détourné pour envoyer des données sensibles via des requêtes d'images.
*   **Liens Hypertextes et Caractères Unicode Invisibles (via Slack) :** Bien que le "link unfurling" ait été désactivé par le fournisseur, l'envoi de liens contenant des données cachées par des caractères Unicode invisibles représente toujours un risque social si l'utilisateur clique dessus, exposant potentiellement les données via l'encodage de l'URL dans les requêtes HTTP.

**Vulnérabilités :**

Les vulnérabilités exploitées sont intrinsèques à la manière dont les agents IA interagissent avec leur environnement et exécutent des tâches, particulièrement lorsque des données non fiables sont traitées sans validation suffisante. L'absence de restriction par défaut sur l'accès à internet et la confiance implicite dans l'exécution de tâches déclenchées par des prompts sont des failles majeures. Les vulnérabilités spécifiques ne sont pas référencées par des CVE dans cet article.

**Recommandations Clés :**

*   **Restriction de l'Accès Internet :** Implémenter des contrôles de sécurité pour restreindre l'accès à Internet par défaut et permettre une gestion granulaire des autorisations.
*   **Désactivation du Rendu d'Images et Liens Non Fiables :** Désactiver le rendu automatique d'images Markdown et de liens hypertextes provenant de domaines non fiables dans la boîte de dialogue de l'agent.
*   **Validation des Prompts :** Ne pas se fier uniquement à la capacité du modèle à "bien agir" ; les agents doivent être considérés comme naïfs face à des données non fiables.

Ces failles ont été signalées à Cognition en avril 2025. L'information est rendue publique après 120 jours pour sensibiliser les utilisateurs.

---
[Source](https://embracethered.com/blog/posts/2025/devin-can-leak-your-secrets/){:target="_blank"}
