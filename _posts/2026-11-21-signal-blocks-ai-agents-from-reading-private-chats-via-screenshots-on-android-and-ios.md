---
title: 'Signal Blocks AI Agents From Reading Private Chats via Screenshots on Android and iOS'
date: 2026-11-21
permalink: /posts/2026/11/21/signal-blocks-ai-agents-from-reading-private-chats-via-screenshots-on-android-and-ios/
tags:
- veille-cyber
- hackernews
---
### Protection renforcée de Signal face aux agents IA

Signal déploie une nouvelle fonctionnalité de blocage des captures d'écran par défaut sur Android et iOS pour empêcher les agents d'IA intégrés aux systèmes d'exploitation de lire les conversations privées. Cette mesure répond à la menace que représentent ces systèmes qui « scannent » l'écran pour accéder aux données des utilisateurs, contournant ainsi les garanties de chiffrement de l'application.

**Points clés :**
*   **Risque d'exfiltration :** Les agents IA peuvent capturer, stocker localement ou transmettre sur des serveurs distants les informations affichées à l'écran, échappant au contrôle de Signal.
*   **Vulnérabilités de permission :** Les agents IA exploitent souvent des permissions système larges (accessibilité, notifications, captures d'écran) accordées initialement par l'utilisateur, comme observé avec l'agent « Muse » de Meta qui a pu lire des messages Signal sans autorisation explicite.
*   **Protection incomplète :** Signal admet que cette mesure est imparfaite, car elle ne protège pas contre d'autres méthodes d'accès plus furtives, telles que la lecture directe des données dans le système de fichiers.

**Recommandations :**
*   **Paramétrage :** Les utilisateurs peuvent gérer ces options dans *Paramètres > Confidentialité > Sécurité de l'application* (activer « Blocage Siri AI » sur iOS ou « Sécurité de l'écran » sur Android).
*   **Appel aux développeurs OS :** Signal presse Apple et Google de fournir des outils standardisés permettant aux développeurs d'exclure facilement leurs applications de l'accès aux données par les IA sans dégrader l'expérience utilisateur.
*   **Vigilance :** Il est conseillé de vérifier les autorisations d'accès accordées aux assistants IA dans les réglages système (ex: réglages de « Siri » sur iOS ou « Applications connectées » pour Gemini sur Android).

*Note : Aucune CVE n'est associée à ces incidents, car il s'agit d'une exploitation légitime des fonctionnalités et permissions accordées aux agents IA par les systèmes d'exploitation eux-mêmes.*

---
[Source](https://thehackernews.com/2026/11/signal-blocks-ai-agents-from-reading.html){:target="_blank"}
