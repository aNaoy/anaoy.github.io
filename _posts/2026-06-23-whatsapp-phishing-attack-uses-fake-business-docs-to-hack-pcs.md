---
title: 'WhatsApp phishing attack uses fake business docs to hack PCs'
date: 2026-06-23
permalink: /posts/2026/06/23/whatsapp-phishing-attack-uses-fake-business-docs-to-hack-pcs/
tags:
- veille-cyber
- bleepingcomp
---
### Campagne mondiale de phishing via WhatsApp : détournement d'outils d'administration légitimes

Une campagne de logiciels malveillants cible actuellement les utilisateurs de WhatsApp à travers le monde en utilisant des comptes compromis pour diffuser des fichiers VBScript dissimulés sous forme de documents professionnels (factures, rapports financiers). L'exécution de ces fichiers permet aux attaquants d'installer silencieusement une version légitime de *ManageEngine Endpoint Central* afin de prendre le contrôle total des systèmes infectés.

**Points clés :**
* **Vecteur d'attaque :** Messages WhatsApp contenant des scripts VBS malveillants, envoyés par des contacts de confiance dont le compte a été piraté.
* **Mécanisme :** Le script modifie le Registre Windows pour contourner le contrôle de compte d'utilisateur (UAC), télécharge et installe un outil d'administration à distance (RMM).
* **Portée :** Campagne internationale (Brésil, Inde, Mexique, Singapour, Europe, etc.).
* **Attribution :** Des liens potentiels avec les groupes ValleyRAT et Gh0st RAT, bien que les preuves soient insuffisantes pour une certitude totale.

**Vulnérabilités exploitées :**
* Aucune CVE spécifique n'est mentionnée, car l'attaque repose sur l'ingénierie sociale et l'utilisation détournée d'un outil légitime (ManageEngine) plutôt que sur une faille logicielle directe.
* **Risque critique :** Contournement des protections UAC par modification du Registre pour l'installation silencieuse de logiciels.

**Recommandations :**
* **Vigilance accrue :** Ne jamais exécuter de fichiers reçus via WhatsApp, même s'ils proviennent d'un contact connu, sans avoir vérifié leur authenticité par un autre canal.
* **Analyse systématique :** Scanner systématiquement tout fichier téléchargé avec une solution antivirus à jour avant toute exécution.
* **Gestion des privilèges :** Surveiller les installations inattendues de logiciels de gestion à distance (RMM) sur les postes de travail.
* **Sensibilisation :** Informer les utilisateurs sur les risques liés aux scripts (fichiers .vbs) et aux documents non sollicités.

---
[Source](https://www.bleepingcomputer.com/news/security/whatsapp-phishing-attack-uses-fake-business-docs-to-hack-pcs/){:target="_blank"}
