---
title: 'Noisy Bear Targets Kazakhstan Energy Sector With BarrelFire Phishing Campaign'
date: 2025-09-06
permalink: /posts/2025/09/06/noisy-bear-targets-kazakhstan-energy-sector-with-barrelfire-phishing-campaign/
tags:
- veille-cyber
- hackernews
---
**Opération BarrelFire : Vague de Phishing Ciblant le Secteur Énergétique Kazakh**

Un groupe d'acteurs malveillants, potentiellement d'origine russe et nommé Noisy Bear, a lancé la campagne "Operation BarrelFire" visant les employés du secteur de l'énergie au Kazakhstan, notamment chez KazMunaiGas (KMG). L'objectif est de dérober des informations et de déployer des implants malveillants. Les attaques ont débuté en avril 2025 et ont ciblé spécifiquement les employés de KMG en mai 2025.

La méthode d'infection commence par un email de phishing contenant une pièce jointe ZIP. Celle-ci inclut un fichier raccourci Windows (LNK), un document factice relatif à KMG, et un fichier texte avec des instructions en russe et kazakh pour exécuter un programme intitulé "KazMunayGaz_Viewer". L'email semble provenir d'un employé du département financier de KMG, mimant une communication officielle interne concernant des mises à jour de politiques, des procédures de certification ou des ajustements salariaux.

Une fois le fichier LNK activé, il dépose des charges utiles supplémentaires, dont un script batch qui facilite le déploiement d'un chargeur PowerShell nommé DOWNSHELL. L'attaque culmine avec le déploiement d'un implant basé sur une DLL, un exécutable 64 bits capable de lancer un shell inversé. L'infrastructure utilisée pour ces attaques est hébergée par Aeza Group, un fournisseur de services d'hébergement "bulletproof" basé en Russie et sanctionné par les États-Unis en juillet 2025 pour son implication dans des activités malveillantes.

Parallèlement, des campagnes ciblant l'Ukraine et la Pologne depuis avril 2025 ont été attribuées à un groupe lié à la Biélorussie, connu sous le nom de Ghostwriter. Ces attaques utilisent des archives ZIP et RAR non autorisées contenant des feuilles de calcul XLS avec des macros VBA. Ces macros déploient et chargent une DLL qui collecte des informations sur les systèmes compromis et télécharge des malwares supplémentaires depuis des serveurs de commande et de contrôle (C2). Des variations ont été observées, utilisant des fichiers Microsoft Cabinet (CAB) aux côtés des raccourcis LNK pour extraire et exécuter la DLL. Dans certains cas, Slack est utilisé comme mécanisme de balisage et d'exfiltration de données. La DLL peut également charger un Cobalt Strike Beacon pour des activités post-exploitation. Ces adaptations suggèrent une volonté de contourner les détections, tout en maintenant la continuité des opérations.

Des cyberattaques ont également été signalées contre la Russie. Le groupe OldGremlin a relancé ses attaques d'extorsion contre des entreprises industrielles russes au premier semestre 2025, en utilisant des emails de phishing pour déployer des malwares et en exploitant la technique "bring your own vulnerable driver" (BYOVD) pour désactiver les solutions de sécurité. Un nouveau logiciel espion nommé Phantom Stealer, basé sur Stealerium, a été distribué via des emails de phishing ciblant la Russie, collectant des informations sensibles et disposant d'un module "PornDetector" pour capturer des captures d'écran de webcam lors de la visite de sites pornographiques, potentiellement utilisé pour des campagnes de "sextorsion". D'autres groupes, tels que Cloud Atlas, PhantomCore et Scaly Wolf, ont également ciblé des organisations russes pour collecter des informations sensibles et déployer des charges utiles additionnelles. Une nouvelle menace Android, se faisant passer pour un outil antivirus des services de sécurité russes (FSB) ou la Banque Centrale russe, a été découverte en janvier 2025, ciblant spécifiquement des représentants d'entreprises russes pour exfiltrer des données et enregistrer les frappes clavier.

**Points Clés :**

*   **Acteurs Malveillants :** Noisy Bear (potentiellement russe), Ghostwriter (lié à la Biélorussie), OldGremlin, Cloud Atlas, PhantomCore, Scaly Wolf.
*   **Campagnes :** Operation BarrelFire (Noisy Bear), campagnes de Ghostwriter, attaques d'OldGremlin, activités de Cloud Atlas, PhantomCore, Scaly Wolf, nouvelle menace Android.
*   **Secteurs Ciblés :** Secteur de l'énergie au Kazakhstan (KazMunaiGas), Ukraine, Pologne, entreprises industrielles russes, entreprises russes en général.
*   **Méthodes d'Attaque :** Phishing par email avec pièces jointes ZIP/LNK, macros VBA dans des documents Office, archives ZIP/RAR, utilisation de scripts PowerShell, malwares basés sur DLL, logiciels espions (infostealers), utilisation de services d'hébergement "bulletproof", utilisation de Slack comme canal C2/exfiltration, technique BYOVD, malwares Android.
*   **Malwares Identifiés :** DOWNSHELL (PowerShell loader), implants DLL, Cobalt Strike Beacon, Phantom Stealer (basé sur Stealerium), VBShower, PhantomRAT, PhantomRShell.
*   **Objectifs :** Dérober des informations sensibles, déployer des implants pour une exploitation ultérieure, extorsion, sextorsion.
*   **Infrastructure :** Aeza Group (hébergement "bulletproof" russe).

**Vulnérabilités :**

*   Aucune vulnérabilité spécifique avec numéro CVE n'est explicitement mentionnée dans l'article. Cependant, l'utilisation de macros VBA dans les documents Office et les fichiers LNK peut être considérée comme des vecteurs d'attaque exploitant la confiance des utilisateurs ou des configurations par défaut permissives. L'exploitation de pilotes vulnérables (BYOVD) par OldGremlin est une technique exploitant des failles de sécurité dans les systèmes d'exploitation ou les pilotes tiers.

**Recommandations (implicites basées sur les descriptions des attaques) :**

*   **Sensibilisation des employés :** Formation continue à la reconnaissance des emails de phishing, à la prudence avec les pièces jointes et les liens suspects.
*   **Sécurité des points d'extrémité :** Mise à jour régulière des logiciels antivirus et des systèmes d'exploitation, activation des protections contre les malwares et les scripts potentiellement dangereux.
*   **Gestion des macros :** Configuration stricte des paramètres des macros dans les applications Office pour limiter leur exécution automatique.
*   **Surveillance du réseau :** Surveillance du trafic réseau pour détecter les communications inhabituelles avec des serveurs C2 connus ou suspects.
*   **Gestion des privilèges :** Application du principe du moindre privilège pour limiter l'impact d'une compromission.
*   **Sécurisation de l'infrastructure :** Utilisation de solutions de sécurité robustes et à jour.
*   **Hébergement et infrastructure :** Éviter l'utilisation de services d'hébergement connus pour leur tolérance aux activités malveillantes.
*   **Analyse et veille :** Maintenir une veille sur les nouvelles menaces, les tactiques, techniques et procédures des groupes d'acteurs malveillants.

---
[Source](https://thehackernews.com/2025/09/noisy-bear-targets-kazakhstan-energy.html){:target="_blank"}
