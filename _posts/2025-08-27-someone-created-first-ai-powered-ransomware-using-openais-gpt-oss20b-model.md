---
title: 'Someone Created First AI-Powered Ransomware Using OpenAIs gpt-oss:20b Model'
date: 2025-08-27
permalink: /posts/2025/08/27/someone-created-first-ai-powered-ransomware-using-openais-gpt-oss20b-model/
tags:
- veille-cyber
- hackernews
---
## Premiers Ransomwares Propulsés par l'IA : PromptLock et ses Implications

Une nouvelle menace baptisée PromptLock a été découverte, marquant la première utilisation connue de l'intelligence artificielle pour générer des variantes de ransomware. Ce logiciel malveillant, écrit en Golang, exploite le modèle gpt-oss:20b d'OpenAI, exécuté localement via l'API Ollama. Le modèle linguistique en source ouverte, récemment publié par OpenAI, permet à PromptLock de créer des scripts Lua dynamiquement pour localiser les fichiers du système, les examiner, exfiltrer des données sélectionnées et procéder au chiffrement.

Ces scripts Lua sont conçus pour être multiplateformes, fonctionnant ainsi sur Windows, Linux et macOS. PromptLock intègre également la capacité de générer une note de rançon personnalisée en fonction des fichiers affectés et du type de machine compromise, qu'il s'agisse d'un ordinateur personnel, d'un serveur d'entreprise ou d'un contrôleur de distribution d'énergie. Les artefacts de PromptLock ont été détectés comme étant téléversés depuis les États-Unis le 25 août 2025, bien que l'identité des créateurs reste inconnue.

La nature dynamique des scripts générés par l'IA complique la détection, car les indicateurs de compromission peuvent varier à chaque exécution. Actuellement considéré comme une preuve de concept plutôt qu'un malware pleinement opérationnel, PromptLock utilise l'algorithme de chiffrement SPECK 128 bits pour verrouiller les fichiers. Des analyses suggèrent également un potentiel d'exfiltration ou de destruction de données, bien que cette dernière fonctionnalité ne soit pas encore pleinement implémentée. Il est à noter que le ransomware ne télécharge pas le modèle AI entier, mais peut s'interfacer avec un serveur exécutant l'API Ollama via un proxy.

L'apparition de PromptLock illustre la facilité croissante avec laquelle les cybercriminels, y compris ceux moins expérimentés techniquement, peuvent rapidement déployer de nouvelles campagnes, développer des malwares et créer du contenu de phishing convaincant. Ceci fait écho à des révélations antérieures concernant l'utilisation de chatbots IA pour des vols de données massifs et le développement de ransomwares sophistiqués.

### Points Clés :

*   **Innovation IA dans le Ransomware :** PromptLock est le premier ransomware connu à utiliser l'IA pour générer dynamiquement des scripts d'attaque.
*   **Modèle Technique :** Utilise le modèle gpt-oss:20b d'OpenAI via Ollama pour créer des scripts Lua.
*   **Fonctionnalités :** Énumération du système de fichiers, exfiltration de données, chiffrement (SPECK 128 bits), génération de notes de rançon personnalisées.
*   **Multiplateforme :** Les scripts Lua générés sont compatibles avec Windows, Linux et macOS.
*   **Défis de Détection :** La nature dynamique des scripts rend l'identification des menaces plus complexe.
*   **Potentiel d'Abus :** Facilite la création de malwares et de campagnes d'hameçonnage pour des individus moins qualifiés techniquement.

### Vulnérabilités :

*   Aucune vulnérabilité spécifique avec un identifiant CVE n'est mentionnée dans l'article pour PromptLock lui-même. L'article souligne cependant la généralité de la vulnérabilité des modèles d'IA aux attaques par "prompt injection", qui peuvent conduire à la divulgation d'informations, à l'exfiltration de données ou à l'exécution de code. L'attaque PROMISQROUTE est également citée, exploitant le routage des modèles pour contourner les filtres de sécurité.

### Recommandations :

*   **Surveillance Continue :** Les chercheurs en cybersécurité doivent adapter leurs méthodes de détection pour faire face à la variabilité des IoCs introduite par l'IA.
*   **Renforcement des Garde-fous de l'IA :** Les développeurs de modèles d'IA doivent continuer à améliorer la robustesse des mesures de sécurité et des protections pour contrer les nouvelles formes d'attaques par injection de texte et les contournements.
*   **Sensibilisation :** Il est crucial de sensibiliser à l'utilisation potentielle de l'IA par des acteurs malveillants pour développer des menaces plus avancées et plus difficiles à détecter.

---
[Source](https://thehackernews.com/2025/08/someone-created-first-ai-powered.html){:target="_blank"}
