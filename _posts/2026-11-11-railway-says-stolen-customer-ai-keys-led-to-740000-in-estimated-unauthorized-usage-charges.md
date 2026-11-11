---
title: 'Railway Says Stolen Customer AI Keys Led to $740,000 in Estimated Unauthorized Usage Charges'
date: 2026-11-11
permalink: /posts/2026/11/11/railway-says-stolen-customer-ai-keys-led-to-740000-in-estimated-unauthorized-usage-charges/
tags:
- veille-cyber
- hackernews
---
### Brèche de sécurité chez Railway : 740 000 $ de clés d'IA dérobées

En octobre, la plateforme PaaS Railway a subi une intrusion ayant permis le vol de clés API et d'autres secrets d'environ 100 000 environnements clients. L'attaque, visant prioritairement les clés de services d'IA, a engendré environ 740 000 $ de frais non autorisés.

**Points clés :**
*   **Vecteur d'attaque :** Un exploit « zero-day » d'évasion de système de fichiers dans le moteur de build a permis à l'attaquant d'obtenir des identifiants internes.
*   **Escalade de privilèges :** L'attaquant a exploité une configuration OIDC erronée et des accès SSH pour atteindre les systèmes de gestion de clés (KMS) permettant de déchiffrer les variables d'environnement des clients.
*   **Données compromises :** Clés d'IA, jetons GitHub OAuth, clés d'agents BYOK, ainsi que des secrets cloud, base de données et de paiement.
*   **Réponse de Railway :** La plateforme a pris en charge les frais liés aux fournisseurs refusant le remboursement (ex: OpenRouter, Anthropic) et a réinitialisé les accès.

**Vulnérabilités exploitées :**
*   Évasion de l'isolation du système de fichiers sur les serveurs de build.
*   Configuration OIDC (OpenID Connect) incorrecte dans l'environnement cloud.
*   Excès de confiance dans les identifiants de build (via le système interne Temporal).

**Recommandations pour les utilisateurs :**
*   **Rotation immédiate :** Révoquer et remplacer toutes les clés, secrets et variables d'environnement stockés avant le 21 octobre.
*   **Audit de sécurité :** Vérifier les journaux d'activité (logs) de GitHub, Docker Hub et des autres services liés pour détecter toute activité suspecte.
*   **Accès réseau :** Restreindre l'accès réseau public aux bases de données et services critiques.
*   **Procédure de remboursement :** Si des frais frauduleux ont été constatés, remplir le formulaire de signalement de Railway et contacter le support spécifique au fournisseur d'IA concerné.

---
[Source](https://thehackernews.com/2026/11/railway-says-stolen-customer-ai-keys.html){:target="_blank"}
