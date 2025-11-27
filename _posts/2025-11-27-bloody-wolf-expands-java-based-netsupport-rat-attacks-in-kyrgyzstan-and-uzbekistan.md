---
title: 'Bloody Wolf Expands Java-based NetSupport RAT Attacks in Kyrgyzstan and Uzbekistan'
date: 2025-11-27
permalink: /posts/2025/11/27/bloody-wolf-expands-java-based-netsupport-rat-attacks-in-kyrgyzstan-and-uzbekistan/
tags:
- veille-cyber
- hackernews
---
**Campagne d'hameçonnage : NetSupport RAT ciblant l'Asie Centrale**

Une campagne de cyberattaques, attribuée au groupe malveillant "Bloody Wolf", cible les secteurs financier, gouvernemental et informatique au Kirghizistan et en Ouzbékistan. Les attaques, actives depuis au moins juin 2025, visent à déployer le logiciel malveillant NetSupport RAT.

**Points Clés :**

*   **Ciblage géographique élargi :** Initialement concentrée sur le Kirghizistan, l'activité s'est étendue à l'Ouzbékistan en octobre 2025.
*   **Ingénierie sociale sophistiquée :** Les attaquants usurpent l'identité de ministères officiels, utilisant des documents PDF d'apparence légitime et des noms de domaine similaires.
*   **Chargement via JAR :** Les courriels frauduleux incitent les victimes à cliquer sur des liens qui téléchargent des fichiers "Java Archive" (JAR) malveillants, sous couvert d'une nécessité d'installation de Java Runtime.
*   **Persistence du malware :** Une fois exécuté, le loader NetSupport RAT établit une persistance via des tâches planifiées, des clés de registre Windows ou des scripts de démarrage.
*   **Géolocalisation en Ouzbékistan :** Les attaques en Ouzbékistan intègrent des restrictions de géolocalisation, redirigeant les requêtes externes vers un site légitime, tandis que celles provenant du pays déclenchent le téléchargement du fichier malveillant.
*   **Utilisation d'outils obsolètes :** Les fichiers JAR observés sont basés sur Java 8 (2014) et la version du NetSupport RAT utilisée date d'octobre 2013.

**Vulnérabilités :**

Aucune vulnérabilité spécifique avec un identifiant CVE n'est explicitement mentionnée dans l'article. L'attaque repose principalement sur l'ingénierie sociale et l'exploitation de la confiance des utilisateurs envers les institutions gouvernementales.

**Recommandations :**

*   **Vigilance accrue face aux courriels :** Être extrêmement prudent avec les courriels provenant d'entités gouvernementales ou financières, en particulier ceux demandant des téléchargements ou des installations.
*   **Vérification des sources :** Examiner attentivement les adresses électroniques des expéditeurs et les URL avant de cliquer ou de télécharger des fichiers.
*   **Mises à jour logicielles :** Maintenir les systèmes d'exploitation et les logiciels (y compris Java Runtime) à jour pour corriger les vulnérabilités connues.
*   **Solutions de sécurité :** Utiliser des logiciels antivirus et anti-malware fiables et s'assurer qu'ils sont également maintenus à jour.
*   **Formation des utilisateurs :** Sensibiliser régulièrement les employés aux risques d'hameçonnage et aux techniques d'ingénierie sociale.

---
[Source](https://thehackernews.com/2025/11/bloody-wolf-expands-java-based.html){:target="_blank"}
