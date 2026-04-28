---
title: 'VECT 2.0 Ransomware Irreversibly Destroys Files Over 131KB on Windows, Linux, ESXi'
date: 2026-04-28
permalink: /posts/2026/04/28/vect-20-ransomware-irreversibly-destroys-files-over-131kb-on-windows-linux-esxi/
tags:
- veille-cyber
- hackernews
---
### VECT 2.0 : Un "Ransomware" destructeur par défaut

Le groupe de cybercriminalité VECT 2.0 déploie un logiciel malveillant présenté comme un ransomware, mais qui agit en réalité comme un destructeur de données (wiper). En raison d'une erreur de conception critique dans son implémentation du chiffrement, il est impossible de restaurer les fichiers de plus de 131 Ko, rendant le paiement de la rançon inutile.

**Points clés :**
* **Fonctionnement erroné :** Le malware fragmente les fichiers en quatre parties. Pour les fichiers dépassant 131 Ko, les clés nécessaires au déchiffrement des trois premières parties sont générées, utilisées, puis immédiatement supprimées par le code. Elles ne sont jamais stockées ni transmises.
* **Modèle RaaS :** VECT 2.0 opère sous un modèle de Ransomware-as-a-Service (RaaS) avec un programme d'affiliation et des partenariats stratégiques (notamment avec BreachForums et TeamPCP).
* **Multiplateforme :** Le malware cible Windows, Linux et ESXi, avec des capacités de persistance en mode sans échec (Windows) et de propagation latérale via SSH.
* **Origine suspecte :** L'analyse suggère que les opérateurs sont novices et auraient potentiellement utilisé l'intelligence artificielle pour générer certaines parties du code, expliquant notamment des exclusions géographiques obsolètes (incluant l'Ukraine dans la zone CIS).

**Vulnérabilités :**
* **Défaut de conception cryptographique :** Absence de sauvegarde des *nonces* nécessaires au déchiffrement pour les fichiers volumineux.
* **Faiblesse de chiffrement :** Utilisation d'un chiffrement non authentifié sans protection d'intégrité, contredisant les affirmations du groupe sur l'utilisation de ChaCha20-Poly1305.
* **Note :** Aucune CVE spécifique n'est associée à cet outil malveillant, il s'agit d'une faille de conception interne au logiciel.

**Recommandations :**
* **Prioriser la résilience :** Ne jamais envisager la négociation ou le paiement, car la récupération des données est techniquement impossible.
* **Stratégie de sauvegarde :** Maintenir des sauvegardes hors ligne (offline) immuables et isolées du réseau.
* **Procédures de récupération :** Tester régulièrement les plans de restauration pour garantir une reprise rapide en cas d'incident.
* **Détection :** Renforcer la surveillance sur les activités de persistance (notamment les modifications de registre pour le démarrage en mode sans échec) et les mouvements latéraux SSH.

---
[Source](https://thehackernews.com/2026/04/vect-20-ransomware-irreversibly.html){:target="_blank"}
