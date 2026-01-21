---
title: 'GitLab warns of high-severity 2FA bypass, denial-of-service flaws'
date: 2026-01-21
permalink: /posts/2026/01/21/gitlab-warns-of-high-severity-2fa-bypass-denial-of-service-flaws/
tags:
- veille-cyber
- bleepingcomp
---
**Mises à jour de sécurité GitLab : Contournement de l'authentification à deux facteurs et déni de service corrigés**

GitLab a publié des correctifs pour plusieurs vulnérabilités critiques, notamment un contournement de l'authentification à deux facteurs (2FA) et des failles permettant des attaques par déni de service (DoS).

**Points Clés :**

*   Des correctifs ont été déployés pour les éditions Community et Enterprise de GitLab.
*   L'entreprise recommande fortement aux administrateurs de passer immédiatement aux versions patchées.
*   Les instances auto-hébergées sont concernées, tandis que GitLab.com et les environnements dédiés sont déjà protégés.

**Vulnérabilités Identifiées :**

*   **CVE-2026-0723 :** Une faiblesse dans les services d'authentification de GitLab, due à une valeur de retour non vérifiée, permet de contourner la 2FA en connaissant l'ID du compte de la victime et en soumettant des réponses de périphérique forgées. Le niveau de sévérité est jugé élevé.
*   **CVE-2025-13927 :** Acteurs malveillants non authentifiés peuvent déclencher des conditions de déni de service en envoyant des requêtes malformées contenant des données d'authentification invalides. Ce problème est jugé de haute sévérité.
*   **CVE-2025-13928 :** Exploitation d'une validation d'autorisation incorrecte dans des points d'API pour provoquer un déni de service. La sévérité est également élevée.
*   **CVE-2025-13335 :** Vulnérabilité de déni de service de sévérité moyenne, exploitable via la configuration de documents Wiki malformés qui contournent la détection de cycle.
*   **CVE-2026-1102 :** Vulnérabilité de déni de service de sévérité moyenne, pouvant être exploitée en envoyant des requêtes d'authentification SSH malformées répétées.

**Recommandations :**

*   Mettre à jour immédiatement les installations auto-hébergées de GitLab vers les versions patchées : 18.8.2, 18.7.2, ou 18.6.4.
*   Les utilisateurs de GitLab.com n'ont aucune action à entreprendre car la plateforme est déjà mise à jour.
*   Les clients GitLab Dedicated n'ont pas besoin d'agir.

---
[Source](https://www.bleepingcomputer.com/news/security/gitlab-warns-of-high-severity-2fa-bypass-denial-of-service-flaws/){:target="_blank"}
