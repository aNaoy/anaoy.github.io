---
title: 'Microsoft Takes Down EvilTokens Device-Code Phishing Service Tied to 12,000 Inbox Compromises'
date: 2026-09-22
permalink: /posts/2026/09/22/microsoft-takes-down-eviltokens-device-code-phishing-service-tied-to-12000-inbox-compromises/
tags:
- veille-cyber
- hackernews
---
### Démantèlement de la plateforme de phishing « EvilTokens »

Microsoft, en collaboration avec plusieurs partenaires technologiques et juridiques, a neutralisé « EvilTokens », une plateforme de type Phishing-as-a-Service (PhaaS) exploitant l'intelligence artificielle pour automatiser les comprométions de messageries professionnelles et la fraude financière.

**Points clés :**
*   **Mode opératoire :** La plateforme utilisait l'abus du flux d'autorisation OAuth 2.0 (code d'appareil) pour détourner des sessions authentifiées sans voler de mots de passe.
*   **Rôle de l'IA :** EvilTokens intégrait un chatbot capable d'analyser les boîtes mail compromises, d'identifier des opportunités de fraude (factures, virements), et de rédiger des messages d'usurpation d'identité convaincants.
*   **Impact :** Plus de 12 000 boîtes mail ont été compromises au sein de 10 000 organisations à travers le monde.
*   **Modèle commercial :** Vendu sur Telegram sous forme d'abonnement (environ 500 $/mois + frais d'accès initiaux), le service a généré plus de 1,1 million de dollars de revenus en cryptomonnaies.
*   **Action de justice :** L'opération a permis la saisie de 50 sites et la désactivation de plus de 150 domaines. Deux suspects ont été arrêtés au Royaume-Uni.

**Vulnérabilités exploitées :**
*   Abus du flux **OAuth 2.0 Device Authorization Grant**. Bien qu'il ne s'agisse pas d'une faille logicielle au sens strict, cette fonctionnalité légitime est détournée pour obtenir des jetons d'accès (access tokens) persistants par simple manipulation sociale (l'utilisateur est incité à saisir un code sur un portail Microsoft officiel).

**Recommandations :**
*   **Sensibilisation :** Former les employés à la méfiance envers les demandes invitant à saisir des codes d'appareil sur des portails de connexion, même si l'URL semble légitime.
*   **Gestion des sessions :** Révoquer régulièrement les sessions actives et les jetons OAuth suspects. En cas de suspicion de compromission, une simple réinitialisation du mot de passe est insuffisante ; il faut invalider explicitement les jetons d'accès et les sessions actives.
*   **Surveillance :** Surveiller la création de règles de transfert automatique ou de masquage d'e-mails dans les boîtes de réception, souvent utilisées pour maintenir une persistance discrète.
*   **Sécurisation renforcée :** Appliquer des politiques d'accès conditionnel strictes limitant l'utilisation des flux d'authentification par code d'appareil aux situations strictement nécessaires.

---
[Source](https://thehackernews.com/2026/09/microsoft-takes-down-eviltokens-device.html){:target="_blank"}
