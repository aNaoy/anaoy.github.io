---
title: 'New attack turned Microsoft 365 Copilot into 1-click data theft tool'
date: 2026-06-15
permalink: /posts/2026/06/15/new-attack-turned-microsoft-365-copilot-into-1-click-data-theft-tool/
tags:
- veille-cyber
- bleepingcomp
---
### SearchLeak : Vulnérabilité critique dans Microsoft 365 Copilot

Une faille critique, baptisée **SearchLeak**, permettait l'exfiltration de données sensibles (emails, mots de passe, documents OneDrive/SharePoint) à partir de Microsoft 365 Copilot Enterprise. L'attaque reposait sur un lien malveillant qu'il suffisait à la victime de cliquer pour déclencher, à son insu, une recherche et l'envoi des résultats vers un serveur contrôlé par l'attaquant.

**Points clés de l'attaque :**
*   **Vectorisation :** L'utilisation d'une URL piégée exploitant le paramètre `q` de Copilot pour injecter des instructions de recherche.
*   **Discrétion :** La victime ne voit qu'une interface Copilot en phase de "réflexion", sans aucune indication visuelle de l'exfiltration.
*   **Chaînage complexe :** L'attaque combine une injection de prompt, une condition de compétition (*race condition*) dans le rendu HTML, et une vulnérabilité SSRF (Server-Side Request Forgery) via Bing pour contourner la politique de sécurité du contenu (CSP).

**Vulnérabilité identifiée :**
*   **CVE-2026-42824 :** Classée comme critique. Elle permettait d'utiliser l'infrastructure de Bing comme proxy pour exfiltrer des données directement depuis l'environnement de l'utilisateur.

**Recommandations :**
*   **Action utilisateur :** Aucune. Microsoft a déployé un correctif pour cette vulnérabilité, ne nécessitant aucune intervention de la part des utilisateurs ou des administrateurs système.
*   **Analyse de sécurité :** Cet incident souligne la nécessité pour les entreprises de surveiller non seulement les vecteurs d'attaque classiques (SSRF, injection HTML), mais aussi la manière dont ces failles peuvent être amplifiées par l'intégration croissante des outils d'IA générative dans les environnements de travail.

---
[Source](https://www.bleepingcomputer.com/news/security/new-attack-turned-microsoft-365-copilot-into-1-click-data-theft-tool/){:target="_blank"}
