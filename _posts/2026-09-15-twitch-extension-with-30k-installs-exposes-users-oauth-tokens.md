---
title: 'Twitch extension with 30K installs exposes users’ OAuth tokens'
date: 2026-09-15
permalink: /posts/2026/09/15/twitch-extension-with-30k-installs-exposes-users-oauth-tokens/
tags:
- veille-cyber
- bleepingcomp
---
### Vol de jetons OAuth via l'extension Twitch "JeetBot"

L'extension de navigateur "Twitch Enhanced Viewer | JeetBot", totalisant plus de 30 000 installations sur Chrome et Firefox, détourne les jetons OAuth des utilisateurs. Bien qu'elle soit présentée comme un outil d'optimisation du streaming (blocage de publicités, forçage de la qualité 1080p), elle agit en réalité comme un vecteur d'exfiltration de données vers des serveurs tiers.

**Points clés :**
*   **Mécanisme d'exfiltration :** L'extension intercepte l'en-tête d'autorisation lors de la consultation des flux Twitch et ajoute le jeton OAuth directement dans les paramètres d'URL (`&auth=`) des requêtes redirigées.
*   **Stockage en clair :** Les jetons sont enregistrés dans les journaux (logs) des serveurs proxy opérés par JeetBot, permettant au développeur d'y accéder facilement.
*   **Ciblage :** L'exfiltration se produit sur toutes les chaînes regardées par l'utilisateur, à l'exception d'une liste blanche de dix chaînes russophones codées en dur.
*   **Divulgation trompeuse :** Contrairement à ses promesses de confidentialité sur le Chrome Web Store, l'extension transmet activement des identifiants de session à des services tiers.

**Vulnérabilités :**
*   Absence de CVE spécifique : Il s'agit d'un comportement malveillant intentionnel ("malware") et non d'une faille logicielle classique. La vulnérabilité réside dans la conception délibérée de l'extension permettant le transfert de jetons d'authentification via des requêtes non sécurisées.

**Recommandations :**
*   **Suppression immédiate :** Désinstaller l'extension "Twitch Enhanced Viewer | JeetBot" des navigateurs.
*   **Réinitialisation des sessions :** Se déconnecter de tous les appareils sur Twitch pour invalider les jetons de session potentiellement compromis, puis se reconnecter pour générer de nouveaux identifiants.
*   **Bonnes pratiques de développement :** Ne jamais faire transiter des en-têtes d'authentification ou des jetons via des serveurs proxy tiers pour éviter l'exposition des données sensibles dans les journaux de requêtes.

---
[Source](https://www.bleepingcomputer.com/news/security/twitch-extension-with-30k-installs-exposes-users-oauth-tokens/){:target="_blank"}
