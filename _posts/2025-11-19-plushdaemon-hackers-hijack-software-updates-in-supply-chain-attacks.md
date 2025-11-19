---
title: '‘PlushDaemon’ hackers hijack software updates in supply-chain attacks'
date: 2025-11-19
permalink: /posts/2025/11/19/plushdaemon-hackers-hijack-software-updates-in-supply-chain-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Attaque "PlushDaemon" : Usurpation de Mises à Jour Logicielles

Un groupe de cybercriminels lié à la Chine, connu sous le nom de "PlushDaemon", exploite désormais les mécanismes de mise à jour logicielle pour mener des opérations de cyberespionnage. Depuis 2018, ce groupe cible des individus et organisations aux États-Unis, en Chine, à Taïwan, à Hong Kong, en Corée du Sud et en Nouvelle-Zélande. Les attaques portent sur des fabricants d'électronique, des universités et des installations industrielles.

**Mécanisme d'attaque :**

PlushDaemon compromet d'abord des routeurs, soit en exploitant des vulnérabilités connues, soit en utilisant des mots de passe administrateur faibles. Ils y installent ensuite un implant appelé "EdgeStepper". Cet implant intercepte les requêtes DNS liées aux mises à jour logicielles et les redirige vers une infrastructure malveillante.

Lorsqu'une victime tente de mettre à jour un logiciel, elle télécharge un premier module malveillant (LittleDaemon), déguisé en fichier DLL. Ce dernier contacte le serveur de commande et contrôle pour récupérer un deuxième chargeur malveillant (DaemonicLogistics). Ce dernier est ensuite utilisé pour télécharger et exécuter le principal outil de l'attaquant : la porte dérobée "SlowStepper". Cette dernière permet de collecter des informations système, d'exécuter des commandes, de réaliser des opérations sur les fichiers et d'utiliser des outils espions pour voler des données de navigateur, intercepter des frappes clavier et subtiliser des identifiants.

Les chercheurs ont observé cette méthode d'attaque ciblant notamment les mises à jour du logiciel de saisie Sogou Pinyin, populaire en Chine, mais d'autres produits ont également été affectés. La capacité d'interception des attaquants leur permet de mener ces attaques de manière efficace contre des cibles à l'échelle mondiale.

**Points Clés :**

*   **Acteur de menace :** PlushDaemon (lié à la Chine).
*   **Technique principale :** Hijacking des mises à jour logicielles (attaque de la chaîne d'approvisionnement).
*   **Implant clé :** EdgeStepper (pour la redirection du trafic de mise à jour).
*   **Malware principal :** SlowStepper (porte dérobée pour le cyberespionnage).
*   **Logiciels affectés :** Divers logiciels, y compris Sogou Pinyin et potentiellement des mises à jour de sécurité VPN (comme observé précédemment avec IPany).
*   **Zones géographiques ciblées :** Principalement États-Unis, Chine, Taïwan, Hong Kong, Corée du Sud, Nouvelle-Zélande.
*   **Type de victimes :** Industries manufacturières, universités.

**Vulnérabilités :**

*   Exploitation de vulnérabilités connues sur les routeurs.
*   Utilisation de mots de passe administrateur faibles sur les routeurs.

**(Aucune vulnérabilité spécifique avec un identifiant CVE n'est mentionnée dans l'article pour l'implant EdgeStepper ou la méthode de détournement des mises à jour, mais les faiblesses des routeurs sont la porte d'entrée initiale.)**

**Recommandations :**

*   Sécuriser les routeurs en exploitant les vulnérabilités connues et en utilisant des mots de passe administrateur forts et uniques.
*   Mettre en œuvre des mesures de sécurité pour surveiller l'intégrité des mises à jour logicielles et la fiabilité des sources de téléchargement.
*   Maintenir une vigilance accrue concernant les compromissions de la chaîne d'approvisionnement logicielle.

---
[Source](https://www.bleepingcomputer.com/news/security/plushdaemon-hackers-hijack-software-updates-in-supply-chain-attacks/){:target="_blank"}
