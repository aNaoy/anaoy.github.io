---
title: 'Infostealer Logs Expose Replayable AI Tokens That Can Bypass MFA'
date: 2026-09-09
permalink: /posts/2026/09/09/infostealer-logs-expose-replayable-ai-tokens-that-can-bypass-mfa/
tags:
- veille-cyber
- hackernews
---
### Vol de sessions et "LLMjacking" : les risques liés aux jetons d'authentification IA

Les cybercriminels utilisent des logiciels de vol d'informations (*infostealers* comme Lumma ou Vidar) pour dérober des jetons de session et des clés API. Ces éléments permettent de contourner l'authentification multifacteur (MFA) et d'accéder directement aux comptes de services d'IA (OpenAI, Google Gemini, Anthropic, etc.) sans avoir besoin des identifiants originaux.

**Points clés :**
*   **Rejeu de jetons :** Une fois volés, les jetons (JWT et JWE) peuvent être réutilisés pour usurper l'identité de l'utilisateur légitime via des navigateurs "anti-détection".
*   **LLMjacking :** Les attaquants exploitent les clés API volées pour utiliser les ressources de calcul des victimes, générant des factures importantes pour l'utilisateur légitime, tout en revendant ces accès sur des forums clandestins.
*   **Fuite de données personnelles :** Environ 17,7 % des jetons analysés contiennent des informations identifiables (PII), facilitant ainsi les futures campagnes de phishing ou d'ingénierie sociale.
*   **Économie souterraine :** Un marché noir en pleine expansion propose des abonnements "discount" à des modèles premium et des outils automatisés pour configurer ces accès volés.

**Vulnérabilités :**
*   **Utilisation de jetons persistants :** Les JWT et JWE qui ne sont pas liés à un appareil spécifique restent exploitables tant qu'ils ne sont pas expirés.
*   **Exposition de secrets :** Les clés API (comme les GitHub PAT) sont fréquemment exposées par erreur, permettant une compromission initiale de l'infrastructure cloud.
*   *Note : Aucune CVE spécifique n'est associée, car le problème réside dans le détournement de jetons valides et non dans une faille logicielle intrinsèque.*

**Recommandations :**
*   **Liaison matérielle :** Privilégier les technologies comme les *Device Bound Session Credentials* (DBSC) qui lient cryptographiquement une session à un appareil unique.
*   **Sécurisation des accès :** Utiliser des flux OAuth 2.0 avec des jetons à durée de vie très courte pour limiter la fenêtre d'opportunité en cas de vol.
*   **Contrôle réseau :** Mettre en place des listes d'autorisation IP (IP allowlisting) pour restreindre l'utilisation des jetons à des environnements réseau approuvés.
*   **Surveillance proactive :** Surveiller les comportements anormaux liés aux clés API et détecter la réutilisation de jetons de session.
*   **Hygiène des secrets :** Éviter de stocker des clés API en clair dans le code source ou les environnements de développement et révoquer immédiatement toute clé exposée.

---
[Source](https://thehackernews.com/2026/09/infostealer-logs-expose-replayable-ai.html){:target="_blank"}
