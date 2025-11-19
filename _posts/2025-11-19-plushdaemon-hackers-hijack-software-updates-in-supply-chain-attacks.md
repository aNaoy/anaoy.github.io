---
title: '‘PlushDaemon’ hackers hijack software updates in supply-chain attacks'
date: 2025-11-19
permalink: /posts/2025/11/19/plushdaemon-hackers-hijack-software-updates-in-supply-chain-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Opération "PlushDaemon" : Piratage des Mises à Jour Logicielles

Un groupe de cyberespionnage lié à la Chine, surnommé "PlushDaemon", compromet les infrastructures pour détourner le trafic des mises à jour logicielles via un nouvel implant nommé EdgeStepper. Ce groupe cible depuis 2018 des organisations et individus dans plusieurs pays (États-Unis, Chine, Taïwan, Hong Kong, Corée du Sud, Nouvelle-Zélande) en utilisant des malwares personnalisés, notamment la porte dérobée SlowStepper.

Les attaques de PlushDaemon, qui s'appuient sur des mises à jour logicielles malveillantes depuis 2019, ont affecté des fabricants d'électronique, des universités et des sites de production automobile.

**Mécanisme d'Attaque :**

1.  **Accès Initial :** Les attaquants exploitent des vulnérabilités connues sur les routeurs ou utilisent des mots de passe faibles pour obtenir un accès.
2.  **Implémentation d'EdgeStepper :** L'implant EdgeStepper, développé en Golang, intercepte les requêtes DNS et les redirige vers un serveur malveillant afin de détourner le trafic des mises à jour légitimes.
3.  **Désimination des Malwares :**
    *   Le premier malware, LittleDaemon (un téléchargeur déguisé en DLL), est délivré à la victime lors de sa tentative de mise à jour.
    *   LittleDaemon établit une connexion avec le serveur de l'attaquant pour récupérer DaemonicLogistics.
    *   Ce dernier est ensuite utilisé pour télécharger et exécuter la porte dérobée principale, SlowStepper.

SlowStepper permet aux attaquants de collecter des informations système, d'effectuer des opérations sur les fichiers, d'exécuter des commandes et d'employer des outils d'espionnage pour voler des données, enregistrer les frappes clavier et récupérer des identifiants.

Les chercheurs ont observé des détournements de mises à jour pour le logiciel de saisie Sogou Pinyin, très populaire en Chine, mais d'autres produits ont également été ciblés. Les capacités de "man-in-the-middle" de PlushDaemon sont jugées suffisantes pour compromettre des cibles à l'échelle mondiale.

**Points Clés :**

*   Attaque par la chaîne d'approvisionnement logicielle.
*   Utilisation d'un nouvel implant (EdgeStepper) pour détourner le trafic des mises à jour.
*   Déploiement de plusieurs couches de malwares (LittleDaemon, DaemonicLogistics, SlowStepper).
*   Objectif de cyberespionnage avec vol de données et d'identifiants.
*   Ciblage d'organisations variées dans plusieurs pays.

**Vulnérabilités :**

*   Vulnérabilités sur les routeurs (non spécifiées dans l'article).
*   Mots de passe faibles sur les interfaces d'administration des routeurs.

**Recommandations :**

*   Sécuriser les routeurs avec des mots de passe robustes et uniques.
*   Appliquer les correctifs de sécurité dès qu'ils sont disponibles pour les dispositifs réseau et les logiciels.
*   Mettre en place des mesures de détection et de réponse aux menaces pour identifier les activités suspectes liées aux mises à jour logicielles.
*   Consulter les indicateurs de compromission partagés par les chercheurs pour identifier et bloquer les infrastructures malveillantes utilisées par PlushDaemon.

---
[Source](https://www.bleepingcomputer.com/news/security/plushdaemon-hackers-hijack-software-updates-in-supply-chain-attacks/){:target="_blank"}
