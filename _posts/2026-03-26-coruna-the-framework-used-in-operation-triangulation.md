---
title: 'Coruna: the framework used in Operation Triangulation'
date: 2026-03-26
permalink: /posts/2026/03/26/coruna-the-framework-used-in-operation-triangulation/
tags:
- veille-cyber
- securelist
---
### Coruna : Analyse du framework derrière l'opération Triangulation

Coruna est un kit d'exploitation sophistiqué pour iOS, identifié comme une évolution directe des outils utilisés lors de l'opération Triangulation. Initialement conçu pour l'espionnage, ce framework modulaire est désormais exploité par divers acteurs pour des attaques ciblées, des opérations de type « watering hole » et des activités cybercriminelles.

**Points clés :**
* **Architecture modulaire :** Le framework utilise un système de téléchargement de composants chiffrés et compressés, sélectionnés dynamiquement selon le modèle de CPU, la version d'iOS et le type de matériel.
* **Évolution constante :** Le kit a été mis à jour pour supporter les processeurs récents (A17, M3) et intégrer des vérifications de versions système plus précises, témoignant d'un développement actif et unifié.
* **Chaîne d'infection :** Le processus débute par un « stager » via Safari, qui fingerprint le navigateur pour déployer les exploits RCE (Remote Code Execution) et PAC (Pointer Authentication Code) appropriés, avant de télécharger la charge utile principale et d'exécuter des exploits kernel.
* **Persistance :** Un « launcher » orchestre l'injection de logiciels malveillants, réutilise les accès en mémoire kernel obtenus pour éviter de redéclencher les vulnérabilités, et efface les traces d'exploitation.

**Vulnérabilités exploitées :**
Le framework s'appuie sur plusieurs vulnérabilités, notamment celles initialement découvertes lors de l'opération Triangulation :
* **CVE-2023-32434**
* **CVE-2023-38606**

**Recommandations :**
* **Mises à jour critiques :** L'installation immédiate des dernières mises à jour de sécurité Apple est impérative pour corriger ces vulnérabilités kernel.
* **Vigilance accrue :** La nature modulaire de Coruna facilite son adoption par de nouveaux attaquants ; il est recommandé de maintenir les appareils à jour pour bénéficier des derniers correctifs de sécurité fournis par le constructeur.

---
[Source](https://securelist.com/coruna-framework-updated-operation-triangulation-exploit/119228/){:target="_blank"}
