---
title: 'The EDR blind spot: 3 ways browser attacks evade endpoint telemetry'
date: 2026-10-02
permalink: /posts/2026/10/02/the-edr-blind-spot-3-ways-browser-attacks-evade-endpoint-telemetry/
tags:
- veille-cyber
- bleepingcomp
---
### Les limites de l'EDR face aux menaces basées sur le navigateur

Les solutions de détection et de réponse sur les terminaux (EDR) sont conçues pour repérer des comportements malveillants au niveau du système (exécution de code, persistance, logiciels malveillants). Cependant, dans un environnement professionnel dominé par le SaaS, une part croissante des attaques se déroule exclusivement dans le navigateur, ne générant aucun artefact exploitable par l'EDR.

**Points clés :**
* **Déplacement de la surface d'attaque :** La majorité des workflows d'entreprise (identité, accès SaaS, gestion de fichiers) transitent désormais par le navigateur, faisant de ce dernier le vecteur privilégié des attaquants.
* **Invisible pour l'EDR :** Les actions telles que l'usurpation de jetons OAuth, l'exfiltration de données via des extensions ou le vol de sessions ne créent pas de processus suspects que l'EDR peut bloquer.
* **Complexité des vecteurs :** L'attaque survient souvent avant toute exécution sur l'hôte, rendant les outils traditionnels aveugles aux compromissions initiales.

**Vulnérabilités et vecteurs d'attaque :**
* **Attaques AiTM (Adversary-in-the-Middle) :** Phishing ciblé via des pages de connexion factices capturant les identifiants, les cookies de session et les jetons OAuth (ex: campagne Storm-2755).
* **Extensions malveillantes :** Utilisation d'extensions légitimes détournées ou malveillantes (type assistants IA) pour lire le contenu des pages, les URL visitées et les historiques de chat sans lever d'alerte système.
* **Attaques ClickFix :** Manipulation du contenu web et du presse-papier pour inciter l'utilisateur à exécuter manuellement des commandes malveillantes (ex: campagne TerminalFix).

**Recommandations :**
* **Adopter l'authentification FIDO2/WebAuthn :** Utiliser des méthodes résistantes au phishing pour lier cryptographiquement l'authentification à l'origine légitime.
* **Mettre en place des contrôles au niveau du navigateur :**
    * Déployer des politiques strictes d'autorisation pour les extensions (listes blanches, revue des permissions).
    * Utiliser le filtrage web pour bloquer les destinations malveillantes et restreindre l'accès aux applications SaaS non approuvées.
    * Mettre en œuvre des capacités de DLP (prévention contre la perte de données) pour limiter les téléchargements, les transferts et l'usage du presse-papier vers des destinations non autorisées.
* **Stratégie de défense multicouche :** Ne pas compter uniquement sur l'EDR. La sécurité doit être décomposée en trois couches interconnectées : **le navigateur**, **l'identité/SaaS** et **le terminal**.

---
[Source](https://www.bleepingcomputer.com/news/security/the-edr-blind-spot-3-ways-browser-attacks-evade-endpoint-telemetry/){:target="_blank"}
