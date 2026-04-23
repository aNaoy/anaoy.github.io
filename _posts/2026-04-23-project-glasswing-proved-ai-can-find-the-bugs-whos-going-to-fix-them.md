---
title: 'Project Glasswing Proved AI Can Find the Bugs. Whos Going to Fix Them?'
date: 2026-04-23
permalink: /posts/2026/04/23/project-glasswing-proved-ai-can-find-the-bugs-whos-going-to-fix-them/
tags:
- veille-cyber
- hackernews
---
### L'ère du "Project Glasswing" : L'urgence de la validation autonome face à l'IA

Le projet **Project Glasswing** d'Anthropic, via son modèle "Mythos", marque un tournant dans la cybersécurité : l'IA est désormais capable de découvrir des vulnérabilités complexes, y compris des failles anciennes non détectées par les humains. Cependant, cet outil révèle une faille structurelle majeure : moins de 1 % des vulnérabilités découvertes sont corrigées, créant un fossé insurmontable entre la découverte automatisée et la lenteur des processus de remédiation humains.

**Points clés :**
*   **Vitesse machine vs vitesse calendaire :** Les attaquants utilisent l'IA pour automatiser des chaînes d'exploitation complètes (reconnaissance, compromission, exfiltration) en quelques heures, tandis que les défenseurs opèrent encore sur des cycles de plusieurs jours.
*   **Capacités de l'IA (Mythos) :** Le modèle a démontré sa capacité à enchaîner plusieurs vulnérabilités pour contourner des protections (sandbox), réaliser des escalades de privilèges et cibler des infrastructures critiques, avec un taux de réussite de 72,4 % dans certains environnements (ex: Firefox).
*   **Inadéquation des méthodes actuelles :** Le système traditionnel basé sur des scores CVSS génériques et des tests de pénétration périodiques est devenu obsolète face à l'avalanche de découvertes générées par l'IA.

**Vulnérabilités :**
L'article mentionne des exploits concrets réalisés par le modèle :
*   Enchaînement de 4 failles indépendantes pour contourner le moteur de rendu des navigateurs et le sandboxing OS.
*   Escalade de privilèges locale dans Linux via des conditions de concurrence (*race conditions*).
*   Création d'une chaîne ROP (Return-Oriented Programming) de 20 gadgets visant les serveurs NFS de FreeBSD.
*   *Note : Bien que des CVE spécifiques ne soient pas listées, l'article souligne l'existence de failles vieilles de 27 ans dans OpenBSD.*

**Recommandations :**
Pour survivre à l'ère post-Mythos, les programmes de sécurité doivent pivoter vers une **validation autonome des expositions** :
1.  **Validation axée sur le signal :** Abandonner les tests planifiés pour des tests continus déclenchés par chaque changement dans l'environnement ou chaque nouvelle menace.
2.  **Contextualisation environnementale :** Prioriser les correctifs non pas sur le score CVSS, mais sur l'exploitabilité réelle au sein de votre infrastructure spécifique.
3.  **Boucle de remédiation fermée :** Automatiser le cycle "détection-validation-patch-revalidation" pour éliminer les transferts manuels de tickets, permettant ainsi une réponse à la vitesse de la machine.

---
[Source](https://thehackernews.com/2026/04/project-glasswing-proved-ai-can-find.html){:target="_blank"}
