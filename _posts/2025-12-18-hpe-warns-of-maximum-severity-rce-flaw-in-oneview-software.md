---
title: 'HPE warns of maximum severity RCE flaw in OneView software'
date: 2025-12-18
permalink: /posts/2025/12/18/hpe-warns-of-maximum-severity-rce-flaw-in-oneview-software/
tags:
- veille-cyber
- bleepingcomp
---
**Vulnérabilité Critique dans HPE OneView : Exécution de Code à Distance**

Hewlett Packard Enterprise (HPE) a corrigé une faille de sécurité d'une gravité maximale dans son logiciel de gestion d'infrastructure HPE OneView. Cette vulnérabilité, identifiée comme CVE-2025-37164, permet à des acteurs malveillants non authentifiés d'exécuter du code arbitraire à distance sur les systèmes non mis à jour.

La faille, découverte par le chercheur en sécurité Nguyen Quoc Khanh, affecte toutes les versions de OneView antérieures à la version 11.00. Elle peut être exploitée via des attaques d'injection de code de faible complexité, sans nécessiter d'authentification préalable. HPE n'a pas précisé si cette vulnérabilité a déjà été activement exploitée.

**Points Clés :**

*   **Nature de la vulnérabilité :** Exécution de code à distance (RCE) via injection de code.
*   **Niveau de sévérité :** Maximum.
*   **Impact :** Permet à un attaquant distant non authentifié d'exécuter du code sur le système vulnérable.
*   **Versions affectées :** Toutes les versions de HPE OneView publiées avant la version 11.00.
*   **Complexité de l'exploitation :** Faible.

**Vulnérabilité :**

*   **CVE :** CVE-2025-37164
*   **Type :** Injection de Code (CWE-94) menant à l'exécution de code à distance.

**Recommandations :**

Il n'existe pas de contournements ou d'atténuations pour cette vulnérabilité. HPE recommande aux administrateurs de mettre à jour les systèmes affectés dès que possible.

*   **Mise à jour générale :** Mettre à niveau vers HPE OneView version 11.00 ou une version ultérieure. Ces versions sont disponibles via le HPE Software Center.
*   **Pour les versions 5.20 à 10.20 :** Il est possible de déployer un correctif de sécurité (hotfix). Ce correctif doit être réappliqué après une mise à niveau de la version 6.60 ou ultérieure vers la version 7.00.00, ou après toute opération de réimagerie du HPE Synergy Composer. Des téléchargements spécifiques sont disponibles pour le correctif de l'appliance virtuelle et pour le correctif Synergy via les pages de support dédiées.

---
[Source](https://www.bleepingcomputer.com/news/security/hpe-warns-of-maximum-severity-rce-flaw-in-oneview-software/){:target="_blank"}
