---
title: 'Chinese Threat Actor Uses Leaked DarkSword Kit to Deploy GHOSTBLADE on iOS'
date: 2026-08-03
permalink: /posts/2026/08/03/chinese-threat-actor-uses-leaked-darksword-kit-to-deploy-ghostblade-on-ios/
tags:
- veille-cyber
- hackernews
---
### Expansion de la menace : Le kit d'exploitation DarkSword cible les utilisateurs iOS

Un acteur malveillant sinophone exploite une version publique du kit **DarkSword** pour compromettre des appareils iOS. Initialement utilisé par des entités étatiques, le code source du kit a été divulgué, permettant à divers groupes criminels de multiplier les campagnes de cyberespionnage.

**Points clés :**
* **Vecteur d'attaque :** Utilisation de techniques de *watering hole* via de fausses pages de connexion (AWS, identifiants Apple).
* **Mode opératoire :** La victime accède à un site piégé qui exécute un script JavaScript déclenchant une chaîne d'exploits (DarkSword), aboutissant à l'installation du malware **GHOSTBLADE**.
* **Impact :** GHOSTBLADE permet l'exfiltration de données sensibles : trousseau de clés (*keychain*), identifiants iCloud, mots de passe Wi-Fi et fichiers personnels.
* **Infrastructure :** Une prolifération de panneaux d'administration (DarkSword Admin, Decode Dashboard) a été identifiée, principalement hébergée à Hong Kong et Singapour.
* **Acteurs associés :** Des liens ont été établis avec le groupe **UNC6353** (utilisant également le kit *Coruna*) et des références à une infrastructure nommée « Thorn C2 ».

**Vulnérabilités :**
* Le kit cible spécifiquement les versions **iOS 18.4 à 18.7**. Bien que les vulnérabilités exploitées soient officiellement corrigées, l'utilisation de chaînes d'exploits complètes permet aux attaquants de contourner la sécurité des appareils non mis à jour. (Note : Aucune CVE spécifique n'est mentionnée dans le texte source).

**Recommandations :**
* **Mise à jour immédiate :** Installer systématiquement les dernières versions d'iOS pour bénéficier des correctifs de sécurité colmatant les failles exploitées par DarkSword.
* **Vigilance utilisateur :** Se méfier des pages de connexion aux services (Apple ID, AWS) accessibles via des liens suspects ou des sites web non officiels. Vérifier systématiquement l'URL dans la barre d'adresse avant de saisir des informations d'identification.
* **Hygiène numérique :** Éviter de cliquer sur des contenus provenant de sources inconnues et utiliser l'authentification à deux facteurs (2FA) pour protéger les comptes iCloud et professionnels.

---
[Source](https://thehackernews.com/2026/08/chinese-threat-actor-uses-leaked.html){:target="_blank"}
