---
title: 'Google Chrome may soon block New Tab hijacker extensions by default'
date: 2026-08-02
permalink: /posts/2026/08/02/google-chrome-may-soon-block-new-tab-hijacker-extensions-by-default/
tags:
- veille-cyber
- bleepingcomp
---
### Renforcement de la sécurité contre le détournement des extensions Chrome

Google développe une nouvelle fonctionnalité de sécurité visant à empêcher les logiciels malveillants d'abuser des politiques d'entreprise pour prendre le contrôle du navigateur. Actuellement, des malwares exploitent ces politiques pour forcer l'installation d'extensions modifiant la page "Nouvel onglet" ou le moteur de recherche par défaut, tout en empêchant l'utilisateur de les supprimer.

**Points clés :**
* **Ciblage des environnements "non gérés" :** La protection se concentre sur les PC grand public (Windows et macOS) où aucune autorité de confiance (domaine ou MDM) ne devrait dicter les politiques de navigation.
* **Blocage automatique :** Chrome bloquera systématiquement l'installation d'extensions tentant de détourner les paramètres de recherche ou de page d'accueil via des politiques locales.
* **Protection contre la conversion :** Les extensions installées manuellement ne pourront plus être transformées en extensions "gérées" par des politiques externes.
* **Gestion des exceptions :** Les administrateurs réseau légitimes disposeront d'une option pour désactiver cette protection si des extensions d'entreprise spécifiques nécessitent ces privilèges.

**Vulnérabilités exploitées :**
* Le mécanisme repose sur l'abus des clés de registre ou de configuration locale qui simulent une gestion par un administrateur (politiques "force-install"). Aucun identifiant CVE spécifique n'est associé à cette technique, car il s'agit d'un détournement de fonctionnalité légitime du navigateur.

**Recommandations :**
* **Utilisateurs finaux :** Soyez vigilants face aux messages "Géré par votre organisation" si votre appareil n'appartient pas à une entreprise, car cela indique souvent une compromission par un logiciel publicitaire ou un malware.
* **Administrateurs système :** Surveillez l'état de conformité de vos parcs informatiques via vos solutions MDM pour vous assurer que les politiques de navigateur appliquées correspondent aux déploiements autorisés.
* **Veille :** Bien que cette fonctionnalité soit en cours de déploiement, il est conseillé de maintenir Chrome à jour pour bénéficier de ces protections dès leur intégration dans la version stable.

---
[Source](https://www.bleepingcomputer.com/news/google/google-chrome-may-soon-block-new-tab-hijacker-extensions-by-default/){:target="_blank"}
