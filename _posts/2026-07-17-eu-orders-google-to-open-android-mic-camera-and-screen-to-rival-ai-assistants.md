---
title: 'E.U. Orders Google to Open Android Mic, Camera and Screen to Rival AI Assistants'
date: 2026-07-17
permalink: /posts/2026/07/17/eu-orders-google-to-open-android-mic-camera-and-screen-to-rival-ai-assistants/
tags:
- veille-cyber
- hackernews
---
### L'Union européenne impose l'ouverture de l'écosystème Android aux assistants IA tiers

La Commission européenne a contraint Google à rendre Android interopérable avec les assistants IA concurrents, en application du *Digital Markets Act* (DMA). D'ici août 2027, Google devra permettre à des assistants tiers d'accéder aux fonctionnalités critiques du système, alignant ainsi les capacités des rivaux sur celles de Gemini.

**Points clés :**
*   **Ouverture des fonctionnalités :** Les assistants tiers pourront accéder à la caméra, au microphone, au contenu de l'écran, aux notifications et à l'automatisation des applications (simulation de frappes et clics).
*   **Programme de certification :** Google doit mettre en place un programme « Qualified AI Assistant » pour les fonctionnalités sensibles (accès aux données, intégration système, automatisation). Les critères de sécurité et d'intégrité devront être identiques à ceux appliqués à Gemini.
*   **Partage de données :** Google est également tenu de partager, sous conditions, des données anonymisées sur ses recherches (requêtes, clics, classement) avec des moteurs de recherche et des chatbots concurrents.
*   **Délais :** Les termes du programme de certification sont attendus pour février 2027, pour une mise en œuvre effective en août 2027.

**Vulnérabilités et risques identifiés :**
*   **Injection de prompt indirecte :** L'exposition des notifications et du contenu de l'écran crée un vecteur d'attaque permettant le piratage d'agents IA (comme illustré par des vulnérabilités précédentes sur les utilities Android).
*   **Risque de sécurité des données :** L'accès étendu aux capteurs et aux données personnelles soulève des inquiétudes sur la protection de la vie privée, bien que Google conserve la possibilité de soumettre des preuves de risques graves pour bloquer certains accès.

**Recommandations pour les développeurs d'applications :**
*   **Protection de l'interface :** Les développeurs d'applications Android doivent implémenter des mécanismes pour masquer les vues sensibles afin d'empêcher les assistants tiers (et potentiellement malveillants) de lire ou d'interagir avec des contenus privés affichés à l'écran.
*   **Gestion des accès :** Anticiper les fonctionnalités permettant de bloquer l'automatisation sur certaines parties critiques de l'application avant la sortie de la version bêta d'Android 18.
*   **Conformité :** Les assistants tiers devront se conformer à des exigences strictes de sécurité (renforcement contre les risques « agentiques », minimisation de l'exposition des données) sous peine de révocation par les autorités de certification.

---
[Source](https://thehackernews.com/2026/07/eu-orders-google-to-open-android-mic.html){:target="_blank"}
