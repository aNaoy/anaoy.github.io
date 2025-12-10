---
title: 'Microsoft Patch Tuesday, December 2025 Edition'
date: 2025-12-10
permalink: /posts/2025/12/10/microsoft-patch-tuesday-december-2025-edition/
tags:
- veille-cyber
- krebs
---
## Mises à Jour de Sécurité Microsoft : Décembre 2025

Microsoft a publié des correctifs pour 56 failles de sécurité, dont une zero-day activement exploitée, marquant la dernière série de mises à jour de l'année 2025. Cette année, Microsoft a corrigé un total de 1 129 vulnérabilités, soit une augmentation par rapport à 2024.

**Points Clés :**

*   La mise à jour de décembre 2025 concerne 56 failles de sécurité.
*   Le nombre total de vulnérabilités corrigées par Microsoft en 2025 atteint 1 129.
*   Ceci marque la deuxième année consécutive où Microsoft corrige plus d'un millier de vulnérabilités.

**Vulnérabilités Principales :**

*   **CVE-2025-62221** : Faute d'escalade de privilèges zero-day affectant Windows 10 et versions ultérieures, résidant dans le "Windows Cloud Files Mini Filter Driver". Cette faille est critique car elle touche un composant essentiel aux services de stockage cloud.
*   **CVE-2025-62554** et **CVE-2025-62557** : Deux vulnérabilités critiques touchant Microsoft Office, exploitables simplement en visualisant un e-mail malveillant dans le volet de prévisualisation.
*   **CVE-2025-62562** : Une autre vulnérabilité critique concernant Microsoft Outlook, bien que le volet de prévisualisation ne soit pas un vecteur d'attaque pour celle-ci.
*   **CVE-2025-64671** : Une faille d'exécution de code à distance dans le plugin GitHub Copilot pour Jetbrains, permettant à des attaquants de contourner les mesures de sécurité via le modèle linguistique. Cette vulnérabilité fait partie d'une crise de sécurité plus large ("IDEsaster") touchant plusieurs plateformes d'IA de codage.
*   **CVE-2025-54100** : Une vulnérabilité d'exécution de code à distance dans Windows PowerShell sur Windows Server 2008 et versions ultérieures, permettant à un attaquant non authentifié d'exécuter du code avec les privilèges de l'utilisateur.
*   D'autres vulnérabilités d'escalade de privilèges jugées comme "plus susceptibles d'être exploitées" par Microsoft, incluent :
    *   CVE-2025-62458 (Win32k)
    *   CVE-2025-62470 (Windows Common Log File System Driver)
    *   CVE-2025-62472 (Windows Remote Access Connection Manager)
    *   CVE-2025-59516 (Windows Storage VSP Driver)
    *   CVE-2025-59517 (Windows Storage VSP Driver)

**Recommandations :**

Il est fortement recommandé d'appliquer les mises à jour de sécurité publiées par Microsoft. Les vulnérabilités d'escalade de privilèges, en particulier celles identifiées comme plus susceptibles d'être exploitées, devraient être corrigées rapidement pour prévenir les compromissions d'hôtes. Il est conseillé de consulter les ressources supplémentaires, comme le SANS Internet Storm Center, pour une analyse plus détaillée.

---
[Source](https://krebsonsecurity.com/2025/12/microsoft-patch-tuesday-december-2025-edition/){:target="_blank"}
