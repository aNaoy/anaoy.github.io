---
title: 'WhatsApp VBScript Campaign Uses Fake Documents to Install ManageEngine RMM Tool'
date: 2026-06-23
permalink: /posts/2026/06/23/whatsapp-vbscript-campaign-uses-fake-documents-to-install-manageengine-rmm-tool/
tags:
- veille-cyber
- hackernews
---
### Campagne de malwares via WhatsApp : détournement d'outils RMM

Une campagne de cyberattaques mondiale utilise WhatsApp pour distribuer des fichiers VBScript malveillants. Les attaquants compromettent des comptes WhatsApp pour envoyer à leurs contacts des fichiers piégés déguisés en documents financiers ou professionnels. Une fois exécuté, le script télécharge et installe à l'insu de l'utilisateur un logiciel de gestion à distance (RMM) légitime, permettant aux pirates de prendre le contrôle total du système infecté.

**Points clés :**
* **Vecteur d'attaque :** Utilisation de comptes WhatsApp compromis pour propager des fichiers `.vbs` à travers les listes de contacts.
* **Ciblage :** Campagne mondiale touchant notamment la Malaisie, le Brésil, l'Inde, le Royaume-Uni et l'Espagne.
* **Mode opératoire :** Utilisation d'une chaîne d'infection multi-étapes. Le script tente de contourner le contrôle de compte d'utilisateur (UAC) de Windows avant d'installer *ManageEngine RMM Central*.
* **Dissimulation :** Les scripts contiennent des métadonnées et des commentaires en chinois imitant des composants officiels de mise à jour de Microsoft pour tromper la vigilance.
* **Attribution suspectée :** Des liens techniques ont été observés avec les infrastructures utilisées par les malwares **Gh0st RAT** et **ValleyRAT**.

**Vulnérabilités :**
* Aucune CVE spécifique n'est mentionnée, car l'attaque repose sur l'exécution volontaire de scripts malveillants par l'utilisateur (social engineering).
* La vulnérabilité réside dans la confiance accordée aux fichiers reçus via messagerie instantanée et dans l'absence de restriction stricte sur l'exécution des fichiers VBScript par le système.

**Recommandations :**
* **Méfiance accrue :** Ne jamais ouvrir de fichiers aux extensions exécutables ou de scripts (telles que `.vbs`, `.exe`, `.bat`, `.js`, `.ps1`) reçus via messagerie, même s'ils proviennent d'un contact connu.
* **Vérification :** Confirmer systématiquement l'authenticité d'un document inattendu par un autre canal de communication avant toute ouverture.
* **Sécurisation :** Désactiver l'exécution automatique des scripts via les politiques de groupe ou utiliser des solutions de sécurité capables de bloquer l'exécution de processus suspects initiés par des applications de messagerie.

---
[Source](https://thehackernews.com/2026/06/whatsapp-vbscript-campaign-uses-fake.html){:target="_blank"}
