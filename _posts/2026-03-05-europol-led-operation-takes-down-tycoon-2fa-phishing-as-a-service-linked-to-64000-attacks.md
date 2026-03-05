---
title: 'Europol-Led Operation Takes Down Tycoon 2FA Phishing-as-a-Service Linked to 64,000 Attacks'
date: 2026-03-05
permalink: /posts/2026/03/05/europol-led-operation-takes-down-tycoon-2fa-phishing-as-a-service-linked-to-64000-attacks/
tags:
- veille-cyber
- hackernews
---
### Démantèlement du Service de Phishing "Tycoon 2FA" : Une Opération Mondiale contre le Vol d'Identité

Une vaste opération coordonnée, dirigée par Europol, a permis de démanteler "Tycoon 2FA", une plateforme de phishing-as-a-service (PhaaS) particulièrement prolifique. Ce service, accessible par abonnement, facilitait les attaques de type "adversary-in-the-middle" (AitM) à grande échelle, permettant à des cybercriminels d'intercepter les identifiants et les codes d'authentification multi-facteurs (MFA).

Lancé en août 2023, Tycoon 2FA a émergé comme l'une des plus importantes opérations de phishing au monde. Proposé sur des plateformes de messagerie cryptée comme Telegram et Signal, il offrait des fonctionnalités avancées pour la configuration, le suivi et l'amélioration des campagnes de phishing. Le développeur principal, identifié comme Saad Fridi, basé au Pakistan, aurait vendu des accès à ce service pour des sommes allant de 120 $ pour dix jours à 350 $ pour un mois d'accès à un panneau d'administration web.

Ce panneau permettait aux utilisateurs de créer des emails de phishing personnalisés, de configurer la livraison du contenu malveillant via des pièces jointes, de gérer les redirections, et de suivre les tentatives de connexion des victimes. Les informations collectées, y compris les identifiants, les codes MFA et les cookies de session, pouvaient être téléchargées directement ou envoyées en temps réel via Telegram.

L'opération a conduit à la suppression de 330 domaines utilisés pour héberger les pages de phishing et les panneaux de contrôle du service. Selon les estimations, Tycoon 2FA serait à l'origine de plus de 64 000 incidents de phishing, impactant des dizaines de milliers de domaines et générant des millions d'emails de phishing chaque mois. Microsoft, qui suit les opérateurs sous le nom de Storm-1747, a bloqué plus de 13 millions d'emails malveillants liés à ce service en octobre 2025, représentant environ 62% de toutes les tentatives de phishing bloquées par l'entreprise cette année-là.

Les victimes de Tycoon 2FA étaient principalement situées aux États-Unis, suivis du Royaume-Uni, du Canada, de l'Inde et de la France. L'analyse des données a révélé que les comptes ciblés étaient majoritairement des environnements d'entreprise, plutôt que des comptes personnels.

**Points Clés :**

*   **Nature du Service :** Phishing-as-a-Service (PhaaS) spécialisé dans les attaques "adversary-in-the-middle" (AitM).
*   **Fonctionnalités :** Panneau d'administration pour la création, la gestion et le suivi des campagnes de phishing, interception d'identifiants et de codes MFA, collecte de cookies de session.
*   **Ciblage :** Principalement les environnements d'entreprise, mais touchant également les secteurs de l'éducation, de la santé, de la finance et du gouvernement.
*   **Échelle :** Associé à plus de 64 000 incidents de phishing, des millions d'emails malveillants mensuels, et potentiellement près de 100 000 organisations touchées mondialement.
*   **Tactiques :** Utilisation de domaines à courte durée de vie, de techniques d'obfuscation de code, de filtrage anti-bot, et de la technique "ATO Jumping" (utilisation de comptes compromis pour distribuer des liens de phishing).

**Vulnérabilités exploitées :**

*   Technique "Adversary-in-the-Middle" (AitM) permettant l'interception des identifiants et des codes MFA.
*   Vol de cookies de session, permettant de contourner l'authentification même après réinitialisation des mots de passe si les sessions actives ne sont pas révoquées.
*   Exploitation de la confiance des utilisateurs dans les marques légitimes et les contacts de confiance.
*   Aucune CVE spécifique mentionnée dans l'article pour les vulnérabilités directement exploitées par le kit, mais l'efficacité du kit réside dans son architecture et ses méthodes d'attaque sophistiquées.

**Recommandations (implicites et générales issues de l'article) :**

*   **Sensibilisation renforcée :** Informer les utilisateurs sur les techniques de phishing avancées, y compris les attaques AitM.
*   **Vigilance face aux demandes d'identification :** Être particulièrement prudent lors de la saisie d'identifiants et de codes MFA, surtout si la demande semble inhabituelle ou survient après un lien suspect.
*   **Révocation des sessions actives :** En cas de suspicion de compromission, révoquer immédiatement toutes les sessions actives et les tokens associés aux comptes concernés.
*   **Sécurité des emails :** Utiliser des solutions de sécurité email robustes capables de détecter les tentatives de phishing sophistiquées.
*   **Surveillance des activités suspectes :** Mettre en place une surveillance proactive des événements de sécurité, notamment les tentatives de connexion inhabituelles et les activités sur les comptes compromis.

---
[Source](https://thehackernews.com/2026/03/europol-led-operation-takes-down-tycoon.html){:target="_blank"}
