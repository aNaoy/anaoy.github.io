---
title: 'Is AI-Generated Code Secure&#x3f;, (Thu, Jan 22nd)'
date: 2026-01-22
permalink: /posts/2026/01/22/is-ai-generated-code-securex3f-thu-jan-22nd/
tags:
- veille-cyber
- sans-isc
---
**L'IA et la Sécurité du Code : Une Analyse par Bandit**

L'utilisation croissante d'outils d'IA pour générer du code, notamment en Python, soulève des questions quant à leur sécurité intrinsèque. Une analyse menée sur un script Python généré à 99% par IA, intégrant des dépendances, du multithreading et des interactions réseau, révèle plusieurs points d'attention. L'outil d'analyse de sécurité "Bandit" a été utilisé pour examiner ce code de 1500 lignes.

**Points Clés :**

*   Les outils d'IA peuvent produire du code fonctionnel mais avec des implications de sécurité potentielles.
*   L'analyse de sécurité avec des outils comme Bandit est cruciale, même pour le code généré par IA.
*   Le contexte d'exécution du code est déterminant pour évaluer le risque associé aux vulnérabilités identifiées.

**Vulnérabilités Identifiées :**

*   **Utilisation potentielle du module `subprocess` :** Le module `subprocess` peut présenter des risques de sécurité s'il est utilisé pour exécuter des commandes basées sur des entrées non fiables.
    *   **CVE :** Non spécifié directement, mais lié à **CWE-78 (Injection de commandes OS)**.
*   **Analyse de données XML non fiables avec `xml.etree.ElementTree.fromstring` :** Cette méthode est vulnérable aux attaques de type XML (XXE).
    *   **CVE :** Non spécifié directement, mais lié à **CWE-20 (Défaut de validation des données d'entrée)**.
*   **Appels `subprocess` et exécution d'entrées non fiables :** Risque d'exécution de commandes arbitraires si des entrées externes sont utilisées sans validation adéquate.
    *   **CVE :** Non spécifié directement, mais lié à **CWE-78 (Injection de commandes OS)**.
*   **Utilisation de générateurs de nombres pseudo-aléatoires non sécurisés :** Les générateurs standards ne sont pas adaptés à des fins cryptographiques ou de sécurité.
    *   **CVE :** Non spécifié directement, mais lié à **CWE-330 (Utilisation d'une graine ou d'un algorithme cryptographique insuffisant)**.
*   **Détection de blocs `try, except, pass` :** Peut masquer des erreurs importantes, rendant le débogage et la gestion des incidents plus difficiles.
    *   **CVE :** Non spécifié directement, mais lié à **CWE-703 (Erreur de manipulation des exceptions)**.

**Recommandations :**

*   **Inclusion explicite de la sécurité dans les prompts IA :** Lors de la génération de code par IA, il est essentiel de spécifier clairement que la sécurité est une priorité. Des instructions telles que "Traiter toutes les entrées externes comme non fiables", "Valider les types, la longueur et le format des entrées", "Utiliser des listes d'autorisation (allow-lists)", "Éviter les fonctions dangereuses (eval, exec, os.system, shell=True)" et "Prévenir les injections de commandes" sont recommandées.
*   **Utilisation de bibliothèques sécurisées :** Remplacer les fonctions potentiellement dangereuses par leurs équivalents sécurisés (par exemple, utiliser `defusedxml` pour l'analyse XML).
*   **Validation et assainissement des entrées :** Mettre en œuvre des mécanismes robustes pour valider et assainir toutes les données provenant de sources externes.
*   **Analyse régulière du code :** Utiliser des outils d'analyse statique comme Bandit pour identifier et corriger les vulnérabilités, que le code soit généré par IA ou écrit manuellement.
*   **Conscience du contexte d'exécution :** Évaluer le risque des vulnérabilités identifiées en fonction de l'environnement dans lequel le code sera exécuté. Un script interne manipulant des données de confiance présente un risque différent d'une application exposée à Internet.

---
[Source](https://isc.sans.edu/diary/rss/32648){:target="_blank"}
