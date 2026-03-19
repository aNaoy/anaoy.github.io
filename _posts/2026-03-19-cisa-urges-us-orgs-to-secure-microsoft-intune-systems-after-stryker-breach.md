---
title: 'CISA urges US orgs to secure Microsoft Intune systems after Stryker breach'
date: 2026-03-19
permalink: /posts/2026/03/19/cisa-urges-us-orgs-to-secure-microsoft-intune-systems-after-stryker-breach/
tags:
- veille-cyber
- bleepingcomp
---
### Sécurisation des environnements Microsoft Intune face aux menaces persistantes

À la suite de l'attaque menée par le groupe « Handala », lié à l'Iran, contre la société Stryker, la CISA appelle les organisations américaines à renforcer d'urgence la sécurité de leurs outils de gestion de terminaux. Les assaillants ont compromis un compte administrateur pour en créer un nouveau, accédant ainsi à Microsoft Intune pour exfiltrer 50 To de données et réinitialiser à distance près de 80 000 appareils.

**Points clés**
*   **Mode opératoire :** Utilisation d'un compte « Global Administrator » frauduleusement créé après le piratage d'un compte administrateur légitime.
*   **Impact :** Exploitation de la fonction de réinitialisation (« wipe ») native d'Intune pour paralyser massivement le parc informatique de la cible.
*   **Menace :** Le groupe Handala, actif depuis 2023, est spécialisé dans le vol de données et le déploiement de logiciels malveillants destructeurs.

**Vulnérabilités**
*   Aucune CVE spécifique n'est citée ; l'incident résulte d'une exploitation de fonctionnalités légitimes (« Living off the Land ») via une compromission de comptes à hauts privilèges.

**Recommandations**
*   **Principe du moindre privilège :** Appliquer strictement le contrôle d'accès basé sur les rôles (RBAC) pour limiter les permissions au strict nécessaire.
*   **Hygiène des accès privilégiés :** Imposer systématiquement l'authentification multifacteur (MFA) via Microsoft Entra ID, en utilisant les politiques d'accès conditionnel et l'analyse des signaux de risque.
*   **Approbation multi-administrateurs :** Exiger l'accord de plusieurs administrateurs pour les actions sensibles (réinitialisation d'appareils, mises à jour d'applications ou modifications des permissions RBAC).
*   **Sécurité « by design » :** Délaisser la confiance aveugle envers les comptes administrateurs au profit d'un modèle de gouvernance rigoureux des modifications critiques.

---
[Source](https://www.bleepingcomputer.com/news/security/cisa-warns-businesses-to-secure-microsoft-intune-systems-after-stryker-breach/){:target="_blank"}
