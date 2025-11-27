---
title: 'OpenAI discloses API customer data breach via Mixpanel vendor hack'
date: 2025-11-27
permalink: /posts/2025/11/27/openai-discloses-api-customer-data-breach-via-mixpanel-vendor-hack/
tags:
- veille-cyber
- bleepingcomp
---
### Fuite de données clients OpenAI via une faille chez Mixpanel

Une faille de sécurité chez Mixpanel, fournisseur d'analyse tiers utilisé par OpenAI, a entraîné l'exposition de données d'identification limitées concernant certains utilisateurs de l'API d'OpenAI. Cette brèche n'a pas affecté les utilisateurs de ChatGPT ou d'autres produits, ni compromis de données sensibles telles que les conversations, les requêtes API, les mots de passe, les clés API ou les informations de paiement.

La cause de l'incident chez Mixpanel est une campagne de smishing (hameçonnage par SMS) détectée le 8 novembre. OpenAI a été informé des données potentiellement exposées le 25 novembre.

**Points clés :**

*   **Nature de l'incident :** Compromission de données chez un fournisseur tiers (Mixpanel), affectant des informations non sensibles d'utilisateurs de l'API OpenAI.
*   **Produits affectés :** Uniquement les utilisateurs de l'API OpenAI.
*   **Données exposées (potentiellement) :** Nom du compte API, adresse e-mail du compte API, localisation approximative, système d'exploitation et navigateur utilisés, sites référents, identifiants d'organisation ou d'utilisateur associés au compte API.
*   **Données NON exposées :** Conversations, requêtes API, données d'utilisation API, mots de passe, identifiants, clés API, détails de paiement, pièces d'identité gouvernementales.
*   **Impact potentiel des données exposées :** Utilisation potentielle dans des attaques de phishing ou d'ingénierie sociale.
*   **Mesures prises par OpenAI :** Notification des utilisateurs affectés, retrait de Mixpanel des services de production, enquête en cours.
*   **Mesures prises par Mixpanel :** Sécurisation des comptes affectés, révocation des sessions, rotation des identifiants, blocage des adresses IP malveillantes, réinitialisation des mots de passe employés, mise en place de nouveaux contrôles de sécurité.

**Vulnérabilités :**

*   Aucune CVE spécifique n'est mentionnée dans l'article pour l'incident Mixpanel. L'article décrit la cause comme une campagne de "smishing (SMS phishing)".

**Recommandations :**

*   **Vigilance accrue :** Surveiller les messages suspects semblant provenir d'OpenAI, notamment ceux contenant des liens ou des pièces jointes. Vérifier toujours la provenance des communications.
*   **Authentification à deux facteurs (2FA) :** Activer l'authentification à deux facteurs sur les comptes.
*   **Ne pas partager d'informations sensibles :** Ne jamais envoyer de mots de passe, clés API, codes de vérification ou autres informations confidentielles par e-mail, SMS ou chat.
*   **Vérification des communications :** S'assurer que les liens et pièces jointes proviennent de domaines officiels d'OpenAI.

---
[Source](https://www.bleepingcomputer.com/news/security/openai-discloses-api-customer-data-breach-via-mixpanel-vendor-hack/){:target="_blank"}
