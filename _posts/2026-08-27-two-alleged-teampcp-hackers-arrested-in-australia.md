---
title: 'Two Alleged ‘TeamPCP’ Hackers Arrested in Australia'
date: 2026-08-27
permalink: /posts/2026/08/27/two-alleged-teampcp-hackers-arrested-in-australia/
tags:
- veille-cyber
- krebs
---
### Démantèlement du groupe cybercriminel « TeamPCP » en Australie

La police fédérale australienne a arrêté deux hommes, Ruben Thomson (21 ans) et Michael Gaebler (23 ans), membres du groupe « TeamPCP ». Ce collectif est responsable d’une vaste campagne d'attaques sur la chaîne d'approvisionnement logicielle (*supply chain attacks*) ayant touché des milliers d'entreprises mondiales depuis 2025.

**Points clés :**
*   **Mode opératoire :** Le groupe utilisait un ver auto-réplicatif nommé **Shai-Hulud** pour infecter des dépôts de code open source. En compromettant les identifiants de développeurs via le phishing, ils injectaient du code malveillant dans des bibliothèques populaires pour voler des secrets industriels et des clés cloud.
*   **Infrastructures visées :** Les attaques ont notamment compromis **LiteLLM** (passerelle IA) et plus de 3 800 dépôts **GitHub**, exposant les données de 2 500 organisations.
*   **Recrutement et collaboration :** Le groupe fonctionnait comme une communauté de cybercriminels collabos (nommée « Cybercats ») et organisait des concours rémunérés en cryptomonnaies pour inciter les participants à infecter le plus grand nombre de paquets logiciels.
*   **Erreurs d'opsec :** Les suspects ont accumulé des erreurs fatales (utilisation de pseudos liés à leur identité réelle sur des sites de "bug bounty", enregistrement de sociétés avec leurs pseudonymes de hackers, et fuites d'informations sur les réseaux sociaux/forums).

**Vulnérabilités exploitées :**
*   **Phishing d'identifiants :** Vol de jetons d'accès aux dépôts (GitHub, NPM).
*   **Chaîne d'approvisionnement :** Injections malveillantes dans des composants logiciels tiers utilisés par des développeurs de confiance.
*   **Absence de délai de sécurité :** Exploitation de la mise à jour automatique des dépendances logicielles avant détection des malwares.

**Recommandations et mesures correctives :**
*   **Implémentation de délais de sécurité (*Cooldowns*) :** Adoption généralisée d'une période de latence (3 jours préconisés) avant l'intégration automatique de nouvelles mises à jour de paquets (ex: Dependabot sur GitHub), permettant aux outils de sécurité de détecter une compromission éventuelle.
*   **Gestion stricte des accès :** Renforcement de l'authentification multifacteur (MFA) pour tous les comptes liés aux plateformes de développement et aux pipelines CI/CD.
*   **Hygiène numérique :** Vigilance accrue sur les extensions de code installées dans les environnements de développement et audit régulier des dépendances open source.
*   **Séparation des identités :** Nécessité pour les chercheurs en sécurité de cloisonner hermétiquement leurs alias de recherche (bug bounty) de leurs activités personnelles et professionnelles.

---
[Source](https://krebsonsecurity.com/2026/08/two-alleged-teampcp-hackers-arrested-in-australia/){:target="_blank"}
