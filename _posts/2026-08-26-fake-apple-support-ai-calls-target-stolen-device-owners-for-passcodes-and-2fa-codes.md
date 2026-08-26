---
title: 'Fake Apple Support AI Calls Target Stolen-Device Owners for Passcodes and 2FA Codes'
date: 2026-08-26
permalink: /posts/2026/08/26/fake-apple-support-ai-calls-target-stolen-device-owners-for-passcodes-and-2fa-codes/
tags:
- veille-cyber
- hackernews
---
### AnonyMousKIT : La menace du "vishing" automatisé contre les appareils Apple volés

Une nouvelle plateforme de type *Phishing-as-a-Service* (PhaaS), nommée **AnonyMousKIT**, exploite l'intelligence artificielle pour cibler les propriétaires d'appareils Apple volés. L'objectif est de contourner le verrouillage d'activation (*Activation Lock*) en manipulant les victimes pour qu'elles divulguent leurs codes de déverrouillage, leurs identifiants Apple et leurs codes d'authentification à deux facteurs (2FA).

**Points clés :**
* **Fonctionnement automatisé :** La plateforme propose des agents vocaux IA (via le service Vapi) capables d'appeler les victimes en se faisant passer pour le support Apple.
* **Stratégie multicanal :** Les attaques utilisent l'e-mail, le SMS, WhatsApp et des appels vocaux automatisés.
* **Modèle économique :** Il s'agit d'une plateforme commerciale avec abonnements, tarification au crédit et support client, facilitant le vol à grande échelle.
* **Fuite de données :** Une vulnérabilité dans le code source partagé des kits permet un accès HTTP non authentifié à certains répertoires, facilitant la surveillance par les chercheurs.

**Vulnérabilités et vecteurs d'attaque :**
* **Ingénierie sociale :** L'usage d'agents vocaux IA imitant le support Apple pour instaurer la confiance.
* **Exposition de données :** Accès non authentifié via des chemins de fichiers relatifs dans le code source des kits de phishing.
* **Absence de correctif :** Le risque est lié à une faille de conception du kit lui-même, rendant vulnérable chaque nouvelle installation déployée.

**Recommandations :**
* **Sécurisation des accès :** Utiliser des clés de sécurité physiques pour protéger les identifiants Apple. Cela neutralise l'interception en temps réel des codes 2FA, étape finale cruciale de l'attaque.
* **Vigilance accrue :** Garder à l'esprit qu'Apple ne demande jamais de mot de passe, de code de déverrouillage de l'appareil ou de code 2FA par téléphone ou via un lien reçu par message.
* **Signalement :** Transférer tout e-mail ou SMS suspect se faisant passer pour Apple à l'adresse officielle : `reportphishing@apple.com`.

---
[Source](https://thehackernews.com/2026/08/fake-apple-support-ai-calls-target.html){:target="_blank"}
