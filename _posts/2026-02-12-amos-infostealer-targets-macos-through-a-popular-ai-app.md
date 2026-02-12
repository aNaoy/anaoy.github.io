---
title: 'AMOS infostealer targets macOS through a popular AI app'
date: 2026-02-12
permalink: /posts/2026/02/12/amos-infostealer-targets-macos-through-a-popular-ai-app/
tags:
- veille-cyber
- bleepingcomp
---
**La menace AMOS pour les utilisateurs macOS : une exploitation des tendances technologiques**

Le logiciel malveillant AMOS (Atomic MacOS Stealer) représente une menace significative pour les utilisateurs de macOS, agissant comme un composant clé dans une économie criminelle visant la collecte et la monétisation d'identités numériques volées. Plutôt qu'un objectif final, AMOS fonctionne comme un moteur de collecte de données à grande échelle, alimentant les marchés clandestins où les identifiants, sessions et données financières sont vendus pour faciliter des prises de contrôle de comptes, des fraudes et des intrusions ultérieures.

Les campagnes de diffusion d'AMOS exploitent activement les tendances technologiques et les plateformes populaires pour tromper les utilisateurs. La dernière tactique observée implique l'exploitation de l'écosystème de l'assistant personnel IA OpenClaw et ClawHub. Les attaquants ont diffusé des "compétences" (extensions) malveillantes, se faisant passer pour des outils légitimes tels que des utilitaires de cryptomonnaie ou d'intégration Google Workspace. Une fois installées, ces extensions permettent à AMOS de dérober des identifiants, des données de portefeuilles de cryptomonnaies, des sessions de navigateur, des clés SSH et d'autres informations sensibles.

Historiquement, AMOS, apparu vers mai 2023, offrait des fonctionnalités telles que l'exportation de mots de passe du trousseau macOS, le vol de sessions de navigateur, la récupération de données de portefeuilles de cryptomonnaies et des capacités de gestion via un panneau web ou des journaux Telegram. Son coût était d'environ 1000 $ par mois. Les données volées par AMOS sont ensuite vendues sur des marchés clandestins à d'autres cybercriminels spécialisés dans les prises de contrôle de comptes, la fraude financière ou le vol de cryptomonnaies.

D'autres méthodes de diffusion incluent l'utilisation de faux dépôts GitHub imitant des marques logicielles connues, l'exploitation du référencement (SEO poisoning) pour apparaître dans les résultats de recherche et l'incitation des victimes à exécuter des commandes dans le Terminal macOS (techniques de type "ClickFix"). Les attaquants ont également utilisé la fonctionnalité de partage de discussions de ChatGPT pour héberger de faux "guides d'installation" directement sur le domaine de ChatGPT, les promouvant via des publicités ciblées. Les méthodes plus traditionnelles comprennent les liens de phishing, les emails frauduleux, les installateurs "trojanisés" et les publicités malveillantes dirigeant vers des sites miroirs de fournisseurs de logiciels légitimes.

La structure opérationnelle d'AMOS s'inscrit dans un modèle de type "Malware-as-a-Service" (MaaS), où les développeurs fournissent la plateforme du stealer, des mises à jour et l'infrastructure sous forme d'abonnement. Les acteurs malveillants en aval acquièrent ces kits, personnalisent les leursres et les canaux de distribution pour maximiser le volume d'infections, produisant ainsi des données volées (logs de stealer) qui sont un produit de base sur les marchés clandestins. Les distributeurs jouent un rôle clé dans l'évolution des campagnes en choisissant les cibles, les canaux de diffusion et en affinant les techniques d'ingénierie sociale.

**Points Clés :**

*   **Nature des Infostealers :** Ils ne sont pas une fin en soi, mais des composants essentiels d'une économie criminelle qui monétise les identités numériques volées.
*   **Ingénierie Sociale :** Les attaquants exploitent les tendances technologiques (comme l'IA) et les plateformes populaires pour inciter les utilisateurs à exécuter le malware.
*   **Modèle Économique :** Fonctionne comme un écosystème "Malware-as-a-Service" (MaaS), où le développement, la distribution et la monétisation sont des étapes distinctes et spécialisées.
*   **Produit Principal :** Les "logs de stealer" (données volées) sont une marchandise échangée sur les marchés clandestins.
*   **Évolution des Tactiques :** Passage des exploits techniques à l'abus de la confiance des utilisateurs, l'usurpation de marque et l'utilisation de canaux de distribution légitimes.

**Vulnérabilités exploitées :**

Bien qu'aucune vulnérabilité logicielle spécifique (CVE) ne soit explicitement mentionnée dans l'article, les attaques AMOS reposent sur :

*   **La faiblesse de la validation des marchés d'extensions :** Permet l'insertion de logiciels malveillants dans des plateformes d'IA (ex: extensions OpenClaw).
*   **L'ingénierie sociale et l'abus de la confiance des utilisateurs :** Les utilisateurs sont incités à télécharger des malwares déguisés en logiciels légitimes ou à exécuter des commandes potentiellement dangereuses.
*   **L'exploitation des moteurs de recherche et des plateformes de développement :** Le SEO poisoning et les faux dépôts GitHub sont utilisés pour diriger les victimes vers des sources malveillantes.
*   **Les techniques d'exécution basées sur des instructions (ClickFix) :** Les utilisateurs sont trompés pour exécuter eux-mêmes le payload malveillant.

**Recommandations :**

*   **Prudence avec les extensions et les add-ons :** Installer uniquement des extensions et des compléments provenant de sources fiables et vérifiées, surtout pour les applications d'IA et les outils de productivité.
*   **Vérification des sources de téléchargement :** Télécharger les logiciels uniquement depuis les sites officiels des éditeurs ou les App Stores de confiance.
*   **Méfiance face aux installations via le Terminal :** Soyez extrêmement prudent lorsque l'on vous demande d'exécuter des commandes dans le Terminal macOS, surtout si elles proviennent de sources non vérifiées ou d'instructions en ligne.
*   **Sécurité des navigateurs :** Utiliser des extensions de sécurité pour les navigateurs et être vigilant face aux sites web suspects.
*   **Sensibilisation aux campagnes de phishing et de malvertising :** Rester informé des dernières tactiques utilisées par les cybercriminels.
*   **Utilisation d'un logiciel antivirus et anti-malware à jour :** Un bon outil de sécurité peut aider à détecter et supprimer les menaces comme AMOS.
*   **Surveillance des journaux d'infostealer :** Pour les organisations, surveiller les fuites de données et les logs volés sur les marchés clandestins peut aider à anticiper les attaques.

---
[Source](https://www.bleepingcomputer.com/news/security/amos-infostealer-targets-macos-through-a-popular-ai-app/){:target="_blank"}
