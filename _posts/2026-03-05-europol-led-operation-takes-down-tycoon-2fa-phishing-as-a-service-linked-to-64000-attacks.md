---
title: 'Europol-Led Operation Takes Down Tycoon 2FA Phishing-as-a-Service Linked to 64,000 Attacks'
date: 2026-03-05
permalink: /posts/2026/03/05/europol-led-operation-takes-down-tycoon-2fa-phishing-as-a-service-linked-to-64000-attacks/
tags:
- veille-cyber
- hackernews
---
### Démantèlement de Tycoon 2FA : Fin d'une plateforme de phishing massive

Une coalition internationale menée par Europol a neutralisé **Tycoon 2FA**, l'un des services de phishing (PhaaS) les plus prolifiques au monde. Opérant par abonnement sur Telegram et Signal, cette plateforme permettait à des milliers de cybercriminels de mener des attaques d'interception de type *Adversary-in-the-Middle* (AitM) à grande échelle, contournant ainsi la double authentification (MFA).

**Points clés :**
* **Portée des dégâts :** Plus de 64 000 incidents de phishing liés, des dizaines de millions d'emails malveillants par mois et près de 100 000 organisations touchées.
* **Modèle opérationnel :** Le service, attribué au développeur Saad Fridi, offrait un panneau de contrôle complet (templates, suivi des victimes, extraction de cookies de session et de codes MFA en temps réel).
* **Techniques avancées :** Utilisation de domaines éphémères (durée de vie de 24 à 72h), contournement des bots, déguisement en services légitimes (Microsoft 365, Gmail) et technique d'« ATO Jumping » pour propager des liens via des comptes déjà compromis.
* **Impact :** Même avec le MFA activé, les victimes perdaient l'accès à leurs comptes car les attaquants dérobaient les jetons de session actifs, rendant la réinitialisation de mot de passe inefficace sans révocation explicite des jetons.

**Vulnérabilités exploitées :**
L'attaque repose sur l'interception de session (AitM) plutôt que sur une faille logicielle spécifique (CVE). Il s'agit d'une exploitation de la logique des protocoles d'authentification modernes qui font confiance aux cookies de session une fois le MFA validé.

**Recommandations :**
* **Révoquer les sessions actives :** En cas de compromission, la simple réinitialisation du mot de passe ne suffit pas ; il est impératif de révoquer tous les jetons de session et les accès actifs.
* **Adopter l'authentification FIDO2/WebAuthn :** Contrairement au MFA par SMS ou applications de code, les clés de sécurité physiques ou la biométrie (FIDO2) sont résistantes aux attaques AitM car elles sont liées au domaine du site authentifié.
* **Surveillance des accès :** Mettre en place une détection des comportements anormaux liés aux cookies de session et aux connexions provenant d'adresses IP ou d'appareils inhabituels.
* **Sensibilisation :** Former les utilisateurs à vérifier systématiquement l'URL de la page de connexion, malgré le réalisme des interfaces de phishing utilisées par ce type de kits.

---
[Source](https://thehackernews.com/2026/03/europol-led-operation-takes-down-tycoon.html){:target="_blank"}
