---
title: 'Malicious VS Code AI Extensions with 1.5 Million Installs Steal Developer Source Code'
date: 2026-01-26
permalink: /posts/2026/01/26/malicious-vs-code-ai-extensions-with-15-million-installs-steal-developer-source-code/
tags:
- veille-cyber
- hackernews
---
### Extensions VS Code malveillantes compromettent le code source des développeurs

Des chercheurs en cybersécurité ont découvert deux extensions pour Visual Studio Code, présentées comme des assistants de codage basés sur l'IA, qui dérobent en réalité le code source des développeurs pour l'envoyer vers des serveurs en Chine. Ces extensions, qui cumulent 1,5 million d'installations, fonctionnent comme prévu pour ne pas éveiller de soupçons, mais contiennent du code malveillant capable de lire et d'encoder tous les fichiers ouverts et les modifications de code. Elles incluent également une fonctionnalité de surveillance en temps réel pouvant exfiltrer jusqu'à 50 fichiers du workspace et intègrent des SDK commerciaux pour le profilage des utilisateurs.

**Points clés :**

*   Deux extensions VS Code malveillantes (ChatGPT - 中文版 et ChatGPT - ChatMoss) ont été identifiées.
*   Elles totalisent 1,5 million d'installations et sont toujours disponibles sur le Visual Studio Marketplace.
*   Leur fonctionnement est normal en apparence, masquant leur véritable objectif : le vol de code source.
*   Les données volées sont envoyées vers des serveurs basés en Chine.
*   Un suivi en temps réel et un profilage des utilisateurs sont également implémentés.

**Vulnérabilités :**

*   Les extensions exploitent un manque de vigilance des utilisateurs et la confiance accordée aux outils présentés comme bénéfiques.
*   Bien que non liées directement aux extensions, l'article mentionne six vulnérabilités "PackageGate" découvertes dans des gestionnaires de paquets JavaScript (npm, pnpm, vlt, Bun). Ces vulnérabilités permettent de contourner les mesures de sécurité relatives à l'exécution de scripts lors de l'installation de paquets.
    *   **CVE-2025-69264** (Score CVSS: 8.8) - Affecte pnpm.
    *   **CVE-2025-69263** (Score CVSS: 7.5) - Affecte pnpm.

**Recommandations :**

*   Désinstaller les extensions suspectes ou celles dont la provenance n'est pas clairement établie.
*   Être vigilant quant aux extensions installées dans les environnements de développement, même celles qui semblent légitimes.
*   Vérifier régulièrement les packages installés et les éventuels scripts exécutés.
*   Pour les problèmes PackageGate :
    *   Maintenir à jour les gestionnaires de paquets (pnpm, vlt, Bun).
    *   Les projets affectés par les vulnérabilités PackageGate devraient envisager des mesures supplémentaires.
    *   Pour npm, suivre les recommandations de GitHub concernant la sécurité de la chaîne d'approvisionnement (adoption de la publication de confiance, tokens d'accès granulaires avec authentification à deux facteurs).
*   Il est conseillé de désactiver les scripts d'installation automatique et de valider les fichiers de verrouillage ("lockfiles") pour se prémunir contre les attaques de la chaîne d'approvisionnement.

---
[Source](https://thehackernews.com/2026/01/malicious-vs-code-ai-extensions-with-15.html){:target="_blank"}
