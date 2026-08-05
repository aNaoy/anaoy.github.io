---
title: 'Leaked n8n API Tokens Exposed Live Instances to Credential Theft'
date: 2026-08-05
permalink: /posts/2026/08/05/leaked-n8n-api-tokens-exposed-live-instances-to-credential-theft/
tags:
- veille-cyber
- hackernews
---
### Risque d'exposition des instances n8n via des jetons API compromis

Des chercheurs de GitGuardian ont identifié 321 instances n8n accessibles publiquement grâce à des jetons API exposés par inadvertance dans des dépôts GitHub. Cette vulnérabilité permet à des attaquants d'accéder à des données sensibles et de compromettre des systèmes tiers connectés sans avoir recours à l'exploitation de failles logicielles (CVE).

#### Points clés
*   **Vol de jetons :** 4 576 jetons uniques ont été trouvés sur GitHub, dont 321 étaient toujours valides sur des instances accessibles.
*   **Portée étendue :** n8n servant de plateforme d'orchestration, un jeton compromis offre souvent un accès direct aux bases de données, environnements cloud, outils de développement et services d'IA reliés.
*   **Méthodes d'attaque :** Les attaquants utilisent les fonctionnalités natives de l'API REST pour énumérer les flux de travail, extraire des secrets codés en dur ou forcer l'instance à transmettre des identifiants stockés vers un serveur externe.
*   **Permanence des risques :** De nombreux jetons n'ont pas de date d'expiration configurée, ce qui les rend utilisables tant qu'ils ne sont pas manuellement révoqués.

#### Vulnérabilités mentionnées
*   **Exposition de secrets :** Fuite de jetons API dans des fichiers `.env` ou des scripts de configuration (`.claude/settings.json`).
*   **CVE-2025-68613 :** Une vulnérabilité d'injection d'expression (score CVSS 9.9) permettant potentiellement une exécution de code, utilisée dans certaines attaques contre n8n, bien que l'exposition des jetons soit un vecteur d'attaque distinct ne nécessitant aucune exploitation de vulnérabilité.

#### Recommandations
*   **Révocation immédiate :** Annuler tout jeton API trouvé dans le code source ou les historiques de commits.
*   **Rotation des secrets :** Si un jeton a été exposé, considérer que tous les identifiants et services connectés à l'instance n8n sont compromis et procéder à leur rotation immédiate.
*   **Hygiène du code :** Utiliser des outils de détection de secrets pour empêcher le commit de jetons API dans les dépôts (publics ou privés).
*   **Audit d'instance :** Examiner les flux de travail (workflows) pour identifier les secrets codés en dur et limiter les permissions des jetons utilisés par les intégrations.
*   **Sécurisation des accès :** Restreindre l'accès à l'API publique de n8n aux seules adresses IP de confiance et s'assurer que l'instance est à jour pour corriger les vulnérabilités connues.

---
[Source](https://thehackernews.com/2026/08/leaked-n8n-api-tokens-exposed-live.html){:target="_blank"}
