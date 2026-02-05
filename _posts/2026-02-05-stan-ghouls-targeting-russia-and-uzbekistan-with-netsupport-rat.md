---
title: 'Stan Ghouls targeting Russia and Uzbekistan with NetSupport RAT'
date: 2026-02-05
permalink: /posts/2026/02/05/stan-ghouls-targeting-russia-and-uzbekistan-with-netsupport-rat/
tags:
- veille-cyber
- securelist
---
**Stan Ghouls : Une Campagne de Ciblage Sophistiquée Exploitant NetSupport RAT**

Le groupe cybercriminel Stan Ghouls (également connu sous le nom de Bloody Wolf) est actif depuis au moins 2023, menant des attaques ciblées contre des organisations en Russie, au Kirghizistan, au Kazakhstan et en Ouzbékistan. Les secteurs visés sont principalement la fabrication, la finance et l'informatique. Les campagnes de ce groupe sont caractérisées par une préparation minutieuse, des outils sur mesure et une infrastructure dédiée.

**Techniques d'Attaque :**

*   **Vecteur d'Infection Initial :** Le groupe utilise exclusivement le spear-phishing, envoyant des courriels contenant des pièces jointes PDF malveillantes. Ces courriels sont rédigés dans la langue locale des pays ciblés (ex: Ouzbek, Kirghiz).
*   **Charge Utile :** Historiquement, Stan Ghouls utilisait le RAT STRRAT. Plus récemment, il a été observé qu'ils exploitent le logiciel légitime NetSupport RAT pour maintenir le contrôle sur les systèmes compromis.
*   **Charge Malveillante (Loader) :** Le document PDF sert de leurre et contient des liens vers un chargeur malveillant basé sur Java. Ce chargeur a pour fonctions :
    *   Afficher un message d'erreur trompeur pour masquer son fonctionnement.
    *   Vérifier le nombre de tentatives d'installation du RAT pour éviter une détection trop rapide.
    *   Télécharger et installer les composants du RAT NetSupport depuis une infrastructure contrôlée par l'attaquant.
*   **Persistance :** Le RAT NetSupport est configuré pour persister sur le système compromis via trois méthodes : ajout au dossier de démarrage de Windows, enregistrement dans les clés de registre de démarrage automatique, et création de tâches planifiées.
*   **Extension Potentielle vers l'IoT :** Des indices suggèrent que Stan Ghouls pourrait avoir élargi son arsenal pour inclure des malwares ciblant l'infrastructure IoT, notamment des fichiers associés au malware Mirai.

**Vulnérabilités Exploités :**

L'article ne détaille pas de CVE spécifiques liées à des vulnérabilités logicielles exploitées. L'attaque repose principalement sur l'ingénierie sociale (phishing) et l'exploitation de la confiance des utilisateurs envers les logiciels légitimes (NetSupport RAT).

**Points Clés :**

*   **Ciblage Géographique :** Ouzbékistan (prioritaire), Russie, Kazakhstan, et des impacts collatéraux potentiels en Turquie, Serbie, Biélorussie.
*   **Secteurs Visés :** Fabrication industrielle, finance, informatique, gouvernement, logistique, centres médicaux, institutions éducatives.
*   **Volume d'Attaques :** Une cinquantaine de victimes identifiées en Ouzbékistan et dix en Russie, ce qui est considérable pour une campagne ciblée.
*   **Motivations :** Principalement financières, mais le cyberespionnage n'est pas exclu.
*   **Outils Signature :** Chargeurs malveillants personnalisés en Java, exploitation de NetSupport RAT.
*   **Évolution :** Passage de STRRAT à NetSupport RAT, et potentielle incursion dans les malwares IoT (Mirai).

**Recommandations :**

Bien que l'article ne propose pas de recommandations formelles dans une section dédiée, les informations fournies impliquent les mesures de sécurité suivantes :

*   **Sensibilisation et Formation :** Renforcer la formation des employés à la détection des courriels de phishing, y compris les pièces jointes suspectes, et à l'identification des tentatives d'ingénierie sociale.
*   **Filtrage des Courriels :** Utiliser des solutions robustes de filtrage de spam et de détection de malwares pour bloquer les courriels de phishing.
*   **Gestion des Logiciels Légitimes :** Être vigilant quant à l'utilisation de logiciels de prise de contrôle à distance, s'assurer qu'ils sont correctement configurés, sécurisés et utilisés uniquement par du personnel autorisé.
*   **Surveillance et Détection :** Mettre en place des outils de surveillance de réseau et des systèmes de détection d'intrusion pour identifier des activités suspectes.
*   **Mises à Jour et Patchs :** Maintenir tous les systèmes d'exploitation et logiciels à jour pour corriger les vulnérabilités connues, bien que cela ne soit pas l'axe principal de cette campagne.
*   **Analyse des Indicateurs de Compromission (IoCs) :** Utiliser les IoCs fournis dans l'article (listes de fichiers, domaines malveillants) pour la détection et la prévention au sein des infrastructures de sécurité.

---
[Source](https://securelist.com/stan-ghouls-in-uzbekistan/118738/){:target="_blank"}
