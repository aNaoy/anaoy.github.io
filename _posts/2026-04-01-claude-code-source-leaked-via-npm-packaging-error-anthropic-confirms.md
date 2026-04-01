---
title: 'Claude Code Source Leaked via npm Packaging Error, Anthropic Confirms'
date: 2026-04-01
permalink: /posts/2026/04/01/claude-code-source-leaked-via-npm-packaging-error-anthropic-confirms/
tags:
- veille-cyber
- hackernews
---
### Fuite du code source de Claude Code : Erreur de packaging et risques de chaîne d'approvisionnement

Anthropic a confirmé une fuite accidentelle du code source de son assistant « Claude Code » suite à une erreur humaine lors de la publication de la version 2.1.88 sur le registre npm. L'inclusion involontaire de fichiers « source map » a permis d'exposer plus de 500 000 lignes de code, révélant des architectures internes sensibles, des mécanismes de lutte contre le détournement de modèle (poisoning) et des fonctionnalités avancées non documentées (KAIROS, mode « dream » et « Undercover »).

**Points clés :**
*   **Exposition du code :** Le code source détaillé permet désormais aux attaquants d'étudier en profondeur la logique de traitement des contextes et les outils d'orchestration pour concevoir des méthodes de contournement (jailbreak) plus précises.
*   **Attaques par dépendances :** Des acteurs malveillants exploitent cette fuite pour réaliser des attaques par « typosquatting » sur npm, en publiant des paquets aux noms proches de ceux utilisés en interne par Anthropic afin de compromettre les développeurs.
*   **Intoxication des données :** Le code révèle qu'Anthropic injecte des définitions d'outils factices pour empoisonner les données d'entraînement des concurrents tentant de pratiquer le *model distillation*.

**Vulnérabilités :**
*   **Fuite de code via Source Maps :** Exposition du code source complet dans un paquet de production.
*   **Attaque de la chaîne d'approvisionnement (Supply Chain) :** Compromission temporaire via une version malveillante de la bibliothèque `axios` (intégrée dans certaines versions de Claude Code le 31 mars 2026), contenant un cheval de Troie d'accès à distance.
*   **Typosquatting :** Utilisation de paquets npm malveillants (`audio-capture-napi`, `color-diff-napi`, etc.) pour cibler les utilisateurs tentant de compiler le code source.

**Recommandations :**
*   **Audit et mise à jour :** Les utilisateurs ayant installé ou mis à jour Claude Code via npm entre le 31 mars 2026 (00:21 et 03:29 UTC) doivent immédiatement supprimer cette version et réinstaller une version sécurisée.
*   **Rotation des secrets :** Par mesure de précaution, il est vivement conseillé de renouveler toutes les clés API et les identifiants qui auraient pu être utilisés avec les versions compromises.
*   **Vigilance sur les dépendances :** Se montrer extrêmement prudent lors de l'installation de paquets npm liés à l'écosystème Claude Code et vérifier systématiquement l'intégrité des sources pour éviter les attaques par confusion de dépendances.

---
[Source](https://thehackernews.com/2026/04/claude-code-tleaked-via-npm-packaging.html){:target="_blank"}
