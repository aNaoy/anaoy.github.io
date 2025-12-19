---
title: 'Cloud Atlas activity in the first half of 2025: what changed'
date: 2025-12-19
permalink: /posts/2025/12/19/cloud-atlas-activity-in-the-first-half-of-2025-what-changed/
tags:
- veille-cyber
- securelist
---
### Évolution des Tactiques du Groupe Cloud Atlas au Premier Semestre 2025

Le groupe Cloud Atlas, actif depuis 2014 et ciblant principalement l'Europe de l'Est et l'Asie centrale, a continué ses opérations au début de 2025. L'infection initiale se fait généralement par le biais d'e-mails de phishing contenant un document malveillant qui exploite une ancienne vulnérabilité dans l'Éditeur d'équations de Microsoft Office (CVE-2018-0802) pour télécharger et exécuter du code malveillant.

**Points Clés:**

*   **Chaîne d'infection:** Les attaques débutent par un e-mail de phishing avec une pièce jointe DOC(X). L'ouverture du document télécharge un template malveillant d'un serveur distant. Ce template, un fichier RTF, contient un exploit pour l'éditeur de formules, téléchargeant et exécutant un fichier HTML Application (HTA). Le fichier HTA crée ensuite des fichiers VBScript qui constituent le backdoor VBShower.
*   **Implants:** VBShower télécharge et installe d'autres backdoors : PowerShower, VBCloud, et CloudAtlas. Ces implants, bien que présentant des fonctionnalités similaires, offrent des capacités uniques. L'utilisation de services cloud pour la gestion des backdoors est une caractéristique marquante.
*   **Nouveaux Composants:** Les recherches ont mis en évidence de nouvelles fonctionnalités et des adaptations des composants existants. Par exemple, la version actuelle du backdoor VBShower exécute des scripts VB téléchargés indépendamment de leur taille, contrairement aux versions précédentes.

**Vulnérabilités:**

*   **CVE-2018-0802:** Vulnérabilité dans l'Éditeur d'équations de Microsoft Office, exploitée pour la phase initiale d'infection.

**Recommandations:**

Bien que l'article ne fournisse pas une section explicite de "recommandations", il est implicitement recommandé aux organisations :

*   De maintenir à jour les logiciels, notamment Microsoft Office, pour corriger les vulnérabilités connues comme CVE-2018-0802.
*   D'être vigilant face aux e-mails de phishing et d'éviter d'ouvrir les pièces jointes suspectes.
*   De mettre en place des solutions de sécurité robustes pour détecter et bloquer les malwares et les communications avec les serveurs de commande et de contrôle (C2).
*   De surveiller le trafic réseau à la recherche d'indicateurs de compromission (IoCs) tels que les adresses IP et les domaines mentionnés dans le rapport.

**Victimes:**

Les cibles identifiées sont situées en Russie et en Biélorussie, avec une activité observée depuis début 2025. Les secteurs touchés incluent les télécommunications, la construction, les entités gouvernementales et les usines.

**Indicateurs de Compromission:**

Des indicateurs de compromission tels que des hashs de fichiers, des noms de domaines et des adresses IP sont disponibles dans l'article original, permettant aux professionnels de la sécurité d'identifier et de bloquer les activités malveillantes.

---
[Source](https://securelist.com/cloud-atlas-h1-2025-campaign/118517/){:target="_blank"}
