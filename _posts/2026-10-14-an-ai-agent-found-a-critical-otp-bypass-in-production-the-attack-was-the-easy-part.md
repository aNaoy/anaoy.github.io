---
title: 'An AI Agent Found a Critical OTP Bypass in Production. The Attack Was the Easy Part.'
date: 2026-10-14
permalink: /posts/2026/10/14/an-ai-agent-found-a-critical-otp-bypass-in-production-the-attack-was-the-easy-part/
tags:
- veille-cyber
- hackernews
---
### Détection automatisée d'une faille critique de contournement d'authentification

Un agent de test d'intrusion basé sur l'intelligence artificielle a identifié une vulnérabilité critique sur le site de production d'un assureur majeur, permettant de contourner le mécanisme de mot de passe à usage unique (OTP).

**Points clés :**
*   **Capacité de l'IA :** L'agent a réussi à cartographier le flux d'authentification et à valider lui-même la vulnérabilité sans intervention humaine, en utilisant une compréhension approfondie du contexte web.
*   **Limites des tests ponctuels :** La faille a été découverte malgré un test d'intrusion humain réalisé six mois auparavant, illustrant l'incapacité des audits rigides et ponctuels à suivre le rythme des déploiements applicatifs.
*   **Approche « agentique » :** Contrairement aux scanners classiques, l'IA simule le comportement d'un utilisateur réel pour tester des flux complexes (authentification, 2FA) en continu.

**Vulnérabilité identifiée :**
*   **Contournement d'OTP (OTP Bypass) :** Le serveur permettait à l'utilisateur de spécifier, via la requête HTTP, le canal (email/SMS) et l'adresse de destination pour recevoir le code. Le serveur ne vérifiait pas si l'adresse fournie était liée au compte utilisateur cible. Il s'agit d'une faille de logique métier classique, mentionnée dans les guides de tests OWASP.

**Recommandations :**
*   **Validation stricte côté serveur :** Ne jamais se fier aux paramètres fournis par le client pour déterminer la destination d'un code de vérification. L'adresse de réception doit être extraite exclusivement de la base de données après authentification de l'identifiant.
*   **Tests de logique métier :** S'assurer que les audits de sécurité incluent des tests sur les flux métier complexes (récupération de mot de passe, modification de profil, processus de paiement) et pas seulement sur des vulnérabilités techniques standard.
*   **Passage à des tests continus :** Adopter des solutions de test automatisées et récurrentes pour détecter les régressions de sécurité introduites lors des mises à jour fréquentes du code source.

---
[Source](https://thehackernews.com/2026/10/an-ai-agent-found-critical-otp-bypass.html){:target="_blank"}
