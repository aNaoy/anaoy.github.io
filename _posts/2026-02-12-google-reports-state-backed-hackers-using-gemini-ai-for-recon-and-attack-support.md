---
title: 'Google Reports State-Backed Hackers Using Gemini AI for Recon and Attack Support'
date: 2026-02-12
permalink: /posts/2026/02/12/google-reports-state-backed-hackers-using-gemini-ai-for-recon-and-attack-support/
tags:
- veille-cyber
- hackernews
---
## IA Générative : Nouvelles Menaces et Utilisation par des Acteurs Malveillants

Des groupes de cybercriminels étatiques et d'autres acteurs malveillants exploitent de plus en plus les modèles d'intelligence artificielle générative, tels que Gemini de Google, pour améliorer leurs capacités offensives. Ces technologies sont utilisées dans diverses phases du cycle de vie des attaques, allant de la reconnaissance à l'exécution, en passant par la création de campagnes d'information et même le vol de modèles d'IA.

**Points Clés :**

*   **Utilisation par des Acteurs Étatiques :** Le groupe UNC2970, lié à la Corée du Nord, utilise Gemini pour la reconnaissance, l'étude de cibles potentielles (entreprises de cybersécurité et de défense, rôles techniques et salaires) et la création de personnalités de phishing. Ce groupe est connu pour son opération "Dream Job" ciblant les secteurs de l'aérospatiale, de la défense et de l'énergie.
*   **Diversité des Utilisations Malveillantes :** D'autres groupes, notamment des acteurs associés à la Chine (UNC6418, Temp.HEX/Mustang Panda, APT31, APT41, UNC795) et à l'Iran (APT42), utilisent également l'IA générative pour :
    *   Collecter des informations ciblées et des identifiants.
    *   Compiler des dossiers sur des individus et des organisations.
    *   Analyser automatiquement des vulnérabilités et planifier des tests.
    *   Extraire des explications de code et déboguer des exploits.
    *   Développer des outils malveillants comme des web shells et des scanners.
    *   Faciliter l'ingénierie sociale et développer des outils de collecte de données.
*   **Malwares et Kits de Phishing Basés sur l'IA :**
    *   Le malware HONESTCUE utilise l'API de Gemini pour générer du code C# destiné à télécharger et exécuter d'autres malwares, souvent sans laisser de traces sur le disque.
    *   COINBAIT est un kit de phishing généré par IA se présentant comme une plateforme d'échange de cryptomonnaies pour voler des identifiants.
*   **Campagnes de Phishing Sophistiquées :** Des campagnes comme ClickFix utilisent des instructions générées par IA pour distribuer des logiciels espions.
*   **Attaques d'Extraction de Modèles :** Des acteurs ciblent les modèles d'IA pour en extraire des informations et créer des modèles de remplacement. Une attaque à grande échelle a vu Gemini recevoir plus de 100 000 requêtes visant à répliquer ses capacités de raisonnement. Il a été démontré qu'un modèle de remplacement peut atteindre une précision de 80% avec un millier de requêtes.

**Vulnérabilités et Risques Identifiés :**

*   L'utilisation d'IA générative pour la reconnaissance et la planification d'attaques accélère le cycle de vie des cyberattaques.
*   La création de personas de phishing personnalisés et l'identification de cibles "faibles" sont facilitées.
*   Les malwares peuvent externaliser la génération de fonctionnalités grâce aux API d'IA.
*   Les kits de phishing peuvent être rapidement développés et personnalisés.
*   Les techniques d'extraction de modèles peuvent permettre de dupliquer le comportement d'un modèle d'IA propriétaire avec un risque accru de sécurité.
*   La distinction entre recherche professionnelle légitime et reconnaissance malveillante devient floue.

**Recommandations :**

Bien que l'article ne détaille pas de recommandations spécifiques, les implications suggèrent plusieurs pistes pour les organisations :

*   **Surveillance accrue des activités suspectes :** Identifier les schémas d'utilisation inhabituels des outils d'IA, en particulier ceux impliquant des recherches ciblées et des générations de code suspectes.
*   **Renforcement des défenses contre le phishing :** Sensibiliser les utilisateurs aux techniques de phishing de plus en plus sophistiquées.
*   **Sécurisation des API d'IA :** Mettre en place des mesures pour limiter l'exploitation abusive des API d'IA, notamment par la détection de requêtes malveillantes et la protection contre les attaques par extraction de modèles.
*   **Surveillance des vulnérabilités :** Rester vigilant face aux nouvelles vulnérabilités découvertes dans les logiciels, y compris celles qui pourraient être exploitées avec l'aide d'IA (ex: CVE-2025-8088 mentionnée).
*   **Comprendre la nature des attaques par extraction de modèles :** Reconnaître que la protection des poids d'un modèle n'est pas suffisante; le comportement du modèle, révélé par les interactions API, est une source d'information pour les attaquants.

---
[Source](https://thehackernews.com/2026/02/google-reports-state-backed-hackers.html){:target="_blank"}
