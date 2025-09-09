---
title: 'Microsoft September 2025 Patch Tuesday fixes 81 flaws, two zero-days'
date: 2025-09-09
permalink: /posts/2025/09/09/microsoft-september-2025-patch-tuesday-fixes-81-flaws-two-zero-days/
tags:
- veille-cyber
- bleepingcomp
---
**Mises à jour de sécurité Microsoft Septembre 2025 : Corrections de 81 vulnérabilités, dont deux zero-day**

La dernière série de correctifs de sécurité de Microsoft, publiée en septembre 2025, adresse 81 failles, parmi lesquelles deux vulnérabilités zero-day déjà divulguées publiquement. Neuf de ces vulnérabilités sont classées comme "Critiques". Les types de failles corrigées incluent 41 élévations de privilèges, 2 contournements de fonctionnalités de sécurité, 22 exécutions de code à distance, 16 divulgations d'informations, 3 dénis de service et 1 usurpation d'identité.

**Vulnérabilités Zero-Day corrigées :**

*   **CVE-2025-55234 :** Vulnérabilité d'élévation de privilèges dans Windows SMB Server, exploitée via des attaques de relais. L'exploitation permet à un attaquant de réaliser des attaques de relais pour obtenir des privilèges élevés. Microsoft recommande d'activer la signature du serveur SMB et la protection étendue pour l'authentification (EPA), ainsi que l'audit pour vérifier la compatibilité avant l'application complète de ces mesures.
*   **CVE-2024-21907 :** Vulnérabilité de mauvaise gestion des conditions exceptionnelles dans Newtonsoft.Json, intégré à Microsoft SQL Server. L'envoi de données spécialement conçues à la méthode JsonConvert.DeserializeObject peut provoquer une exception StackOverflow et entraîner un déni de service. Un attaquant non authentifié et distant peut potentiellement exploiter cette faille.

**Recommandations :**

La principale recommandation est d'appliquer les mises à jour de sécurité de Microsoft dès que possible pour corriger ces 81 vulnérabilités, en particulier les deux zero-day. L'article mentionne que Windows inclut déjà des paramètres pour renforcer le SMB Server contre les attaques de relais, mais recommande d'activer l'audit pour s'assurer qu'il n'y aura pas de problèmes de compatibilité lors de leur application complète.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-september-2025-patch-tuesday-fixes-81-flaws-two-zero-days/){:target="_blank"}
