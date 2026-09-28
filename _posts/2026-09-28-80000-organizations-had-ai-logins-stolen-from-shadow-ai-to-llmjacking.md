---
title: '80,000+ Organizations Had AI Logins Stolen: From Shadow AI to LLMjacking'
date: 2026-09-28
permalink: /posts/2026/09/28/80000-organizations-had-ai-logins-stolen-from-shadow-ai-to-llmjacking/
tags:
- veille-cyber
- bleepingcomp
---
### La menace invisible : le vol d’identifiants et de sessions IA en entreprise

Une étude de SOCRadar révèle que les identifiants d’outils d'IA sont massivement ciblés par des logiciels malveillants de type « infostealer ». Plus de 80 000 entreprises sont concernées, avec une prédominance marquée pour ChatGPT, bien que les outils de développement (Hugging Face, Replit) soient également visés. Ce phénomène, alimenté par le "Shadow AI" (utilisation d'outils IA sans supervision informatique), transforme les comptes IA en mines d'or pour les attaquants.

**Points clés :**
*   **Risque multidimensionnel :** Un compte IA volé offre un accès immédiat à l'historique des conversations (données confidentielles), aux capacités d'exécution d'agents, aux ressources facturables et aux intégrations tierces (CRM, emails).
*   **Contournement de la MFA :** Le vol de cookies de session permet aux attaquants de s'affranchir de l'authentification multifacteur (MFA). Un simple changement de mot de passe ne suffit pas à expulser l'intrus.
*   **LLMjacking :** Les clés API détournées sont revendues sur le dark web ou utilisées pour exploiter la capacité de calcul des entreprises aux frais des victimes.
*   **Omniprésence :** Le risque touche tous les secteurs, de la technologie à la santé, principalement via des appareils non gérés sur lesquels des employés utilisent leurs emails professionnels.

**Vulnérabilités :**
*   **Sessions persistantes :** La réutilisation de jetons de session (cookies) volés permet de maintenir l'accès malgré la MFA.
*   **Shadow AI :** L'usage non contrôlé d'outils IA par les employés crée une surface d'attaque invisible pour les équipes de sécurité.
*   **Permissions excessives :** Les jetons OAuth accordés aux plateformes d'automatisation (ex: Zapier) permettent aux attaquants de créer des workflows malveillants au sein des systèmes internes.

**Recommandations :**
*   **Centralisation :** Imposer l'utilisation des outils IA via un SSO (Single Sign-On) avec des sessions à courte durée de vie.
*   **Surveillance active :** Détecter les anomalies de connexion (changement de géolocalisation ou d'empreinte appareil en milieu de session) et surveiller l'utilisation suspecte des clés API (horaires atypiques ou ASN inconnus).
*   **Gestion des accès :** Appliquer une rotation régulière des clés API et limiter leurs privilèges au strict nécessaire.
*   **Audit "Shadow AI" :** Identifier les comptes professionnels associés à des outils tiers via une veille sur les logs de vol d'identifiants.
*   **Réaction :** En cas de compromission, invalider immédiatement les sessions, supprimer les méthodes de paiement enregistrées et traiter l'incident au niveau du terminal infecté.

---
[Source](https://www.bleepingcomputer.com/news/security/80-000-plus-organizations-had-ai-logins-stolen-from-shadow-ai-to-llmjacking/){:target="_blank"}
