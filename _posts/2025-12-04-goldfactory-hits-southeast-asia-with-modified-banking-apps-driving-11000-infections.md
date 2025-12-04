---
title: 'GoldFactory Hits Southeast Asia with Modified Banking Apps Driving 11,000+ Infections'
date: 2025-12-04
permalink: /posts/2025/12/04/goldfactory-hits-southeast-asia-with-modified-banking-apps-driving-11000-infections/
tags:
- veille-cyber
- hackernews
---
## GoldFactory : La Nouvelle Vague de Fraude Bancaire Mobile en Asie du Sud-Est

Des cybercriminels associés au groupe dénommé GoldFactory ont lancé une nouvelle campagne d'attaques ciblant les utilisateurs de mobiles en Indonésie, Thaïlande et Vietnam. Depuis octobre 2024, ils propagent des applications bancaires modifiées contenant des malwares pour Android. Ce groupe, actif depuis juin 2023 et d'origine chinoise, est connu pour ses malwares personnalisés tels que GoldPickaxe, GoldDigger et GoldDiggerPlus, ciblant à la fois Android et iOS. GoldFactory semble avoir des liens avec Gigabud, un autre malware Android partageant des tactiques similaires d'usurpation d'identité et de pages d'atterrissage.

Les attaques démarrent en Thaïlande, puis s'étendent au Vietnam et à l'Indonésie. Plus de 300 échantillons d'applications bancaires modifiées ont été identifiés, entraînant plus de 11 000 infections, dont environ 63% en Indonésie.

**Mécanisme d'attaque :**
Les cybercriminels usurpent l'identité d'entités gouvernementales ou de marques locales pour inciter les victimes à installer des malwares via des liens envoyés par messagerie (comme Zalo). Par exemple, ils se font passer pour des compagnies d'électricité pour exiger des paiements sous peine de coupure de service, incitant ensuite les victimes à télécharger une application via Zalo pour "lier leurs comptes".

Ces liens redirigent vers de fausses pages imitant le Google Play Store, déployant des chevaux de Troie d'accès à distance (RAT) comme Gigabud, MMRat ou Remo. Ces malwares exploitent les services d'accessibilité d'Android pour permettre un contrôle à distance, en injectant du code malveillant dans les applications bancaires légitimes sans altérer leur fonctionnement normal.

**Composants techniques clés :**
Trois familles de malwares basées sur des frameworks de hooking ont été identifiées :
*   **FriHook :** Utilise un gadget Frida injecté dans l'application bancaire.
*   **SkyHook :** Emploie le framework public Dobby.
*   **PineHook :** Utilise un framework de hooking basé sur Java, Pine.

Ces frameworks permettent de masquer les applications utilisant les services d'accessibilité, de prévenir la détection de capture d'écran, d'usurper la signature d'une application Android, de dissimuler la source d'installation, de mettre en œuvre des fournisseurs de jetons d'intégrité personnalisés et d'obtenir le solde des comptes victimes.

L'infrastructure malveillante a également révélé une version de test d'un nouveau malware Android, Gigaflower, potentiellement successeur de Gigabud. Ce dernier supporterait 48 commandes, incluant la diffusion en temps réel d'activités de l'appareil, l'utilisation des services d'accessibilité pour le keylogging et la lecture de contenu, la présentation de fausses notifications système pour collecter des informations, et l'extraction de données d'identification à partir d'images via reconnaissance optique de caractères. Une fonctionnalité de scanner de QR codes pour les cartes d'identité vietnamiennes est également en développement.

GoldFactory semble avoir abandonné ses malwares iOS au profit d'une méthode encourageant les victimes à emprunter un appareil Android pour continuer le processus d'infection, probablement en raison des mesures de sécurité renforcées sur iOS.

**Points clés :**
*   Campagne d'attaques orchestrée par le groupe GoldFactory ciblant l'Asie du Sud-Est.
*   Utilisation d'applications bancaires modifiées et de malwares pour Android.
*   Usurpation d'identité d'entités gouvernementales et de marques locales.
*   Exploitation des services d'accessibilité d'Android pour le contrôle à distance.
*   Développement de nouveaux malwares (Gigaflower) et de fonctionnalités avancées.
*   Changement de tactique pour iOS, privilégiant désormais l'utilisation d'appareils Android.

**Vulnérabilités (si applicables) :**
L'article ne mentionne pas de CVE spécifiques. Les vulnérabilités exploitées sont liées à :
*   L'ingénierie sociale pour inciter au téléchargement d'applications non officielles.
*   L'exploitation des services d'accessibilité d'Android.
*   L'injection de code dans des applications légitimes.
*   La capacité à contourner les mesures de sécurité des applications et du système.

**Recommandations :**
*   Ne jamais télécharger d'applications à partir de sources non officielles ou de liens reçus par messagerie.
*   Être vigilant face aux appels téléphoniques suspects ou aux demandes inhabituelles de paiement ou de téléchargement d'applications.
*   Vérifier attentivement les autorisations demandées par les applications, en particulier celles concernant les services d'accessibilité.
*   Maintenir les systèmes d'exploitation mobiles et les applications à jour pour bénéficier des derniers correctifs de sécurité.
*   Sensibiliser les utilisateurs aux tactiques d'ingénierie sociale utilisées par les cybercriminels.

---
[Source](https://thehackernews.com/2025/12/goldfactory-hits-southeast-asia-with.html){:target="_blank"}
