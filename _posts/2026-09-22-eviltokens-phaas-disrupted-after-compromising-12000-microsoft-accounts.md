---
title: 'EvilTokens PhaaS disrupted after compromising 12,000 Microsoft accounts'
date: 2026-09-22
permalink: /posts/2026/09/22/eviltokens-phaas-disrupted-after-compromising-12000-microsoft-accounts/
tags:
- veille-cyber
- bleepingcomp
---
### Démantèlement de la plateforme de phishing EvilTokens

La plateforme de Phishing-as-a-Service (PhaaS) « EvilTokens », opérée par le groupe Storm-2992, a été neutralisée suite à une opération coordonnée par Microsoft, les autorités britanniques et des partenaires en cybersécurité. Ce service, actif depuis février, a permis de compromettre plus de 12 000 comptes Microsoft au sein de 10 000 organisations à travers le monde.

**Points clés :**
*   **Méthodologie :** EvilTokens se spécialise dans le phishing par « code d'appareil » (device-code phishing), détournant le flux d'authentification OAuth 2.0 conçu pour les appareils sans interface de saisie.
*   **Fonctionnalités avancées :** La plateforme intégrait des outils basés sur l'IA pour analyser les boîtes mail compromises, identifier des cibles de haute valeur et automatiser des campagnes de fraude au président (BEC).
*   **Impact :** Environ 97,5 % des comptes compromis appartenaient à des domaines d'entreprise, principalement dans les secteurs de la construction, de la finance, de la santé et de l'éducation.
*   **Modèle économique :** Vendu sur Telegram sous forme d'abonnement (500 $/mois), le kit proposait des options d'évitement (anti-bots, redirections multi-étapes) et des modèles de mails personnalisés.

**Vulnérabilités exploitées :**
*   Le mécanisme d'authentification par **code d'appareil OAuth 2.0** est la faille principale exploitée. Il permet aux attaquants de contourner les protections MFA classiques en incitant les utilisateurs à autoriser un appareil malveillant via un portail de connexion Microsoft légitime. (Il n'existe pas de CVE spécifique, car il s'agit d'un détournement de fonctionnalité légitime).

**Recommandations :**
*   **Désactivation :** Désactiver le flux d'authentification par code d'appareil dans les paramètres de configuration si celui-ci n'est pas strictement nécessaire pour les activités de l'entreprise.
*   **Authentification robuste :** Privilégier l'usage de méthodes d'authentification résistantes au phishing, telles que les clés de sécurité FIDO2 ou les *passkeys*.
*   **Sensibilisation :** Former les utilisateurs à vérifier systématiquement l'application ou le service qui demande une authentification, et à faire preuve de méfiance face aux notifications inattendues.
*   **Surveillance :** Surveiller activement les journaux d'activité de connexion pour détecter des comportements anormaux liés aux jetons d'accès.

---
[Source](https://www.bleepingcomputer.com/news/security/eviltokens-phaas-disrupted-after-compromising-12-000-microsoft-accounts/){:target="_blank"}
