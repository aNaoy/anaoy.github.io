---
title: 'Microsoft fixes streaming issues triggered by Windows updates'
date: 2025-09-10
permalink: /posts/2025/09/10/microsoft-fixes-streaming-issues-triggered-by-windows-updates/
tags:
- veille-cyber
- bleepingcomp
---
**Mises à jour Windows : Résolution des problèmes de diffusion NDI**

Des mises à jour de sécurité de Microsoft publiées en août 2025 ont causé de sévères problèmes de latence et de saccades pour le logiciel de diffusion NDI (Network Device Interface) sur les systèmes Windows 10 et Windows 11. Ces dysfonctionnements ont été signalés par de nombreux utilisateurs sur diverses plateformes.

Les mises à jour spécifiques à l'origine de ces problèmes sont KB5063878 pour Windows 11 24H2 et KB5063709 pour Windows 10 21H2/22H2. Ces correctifs pouvaient entraîner des pertes inattendues de trafic NDI, particulièrement sur les connexions RUDP, tandis que les communications UDP et TCP restaient stables.

Microsoft a déployé de nouvelles mises à jour, KB5065426 et KB5065429, le mardi suivant, pour corriger ce problème connu.

**Points Clés :**

*   Des mises à jour de sécurité Windows d'août 2025 ont perturbé la diffusion NDI.
*   Les symptômes comprenaient une latence élevée, des saccades et une mauvaise qualité audio/vidéo.
*   Les mises à jour affectées étaient KB5063878 et KB5063709.
*   Le problème touchait principalement les connexions NDI utilisant RUDP.

**Vulnérabilités :**

Aucune vulnérabilité de sécurité spécifique (identifiée par un CVE) n'est mentionnée dans l'article comme étant exploitée. Le problème découle d'une incompatibilité introduite par les mises à jour logicielles, impactant la fonctionnalité NDI.

**Recommandations :**

*   **Installer les dernières mises à jour :** Il est recommandé d'installer les mises à jour les plus récentes fournies par Microsoft (KB5065426 et KB5065429 ou ultérieures) pour résoudre le problème de manière permanente.
*   **Solution de contournement temporaire :** Pour ceux qui ne peuvent pas installer immédiatement les mises à jour, il est possible de configurer le mode de réception NDI pour utiliser TCP ou UDP. Cela peut être fait via le gestionnaire d'accès NDI (NDI Access Manager) en sélectionnant "Single TCP or UDP" dans l'onglet "Advanced" après avoir installé le pack NDI Tools.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-fixes-streaming-issues-triggered-by-windows-updates/){:target="_blank"}
