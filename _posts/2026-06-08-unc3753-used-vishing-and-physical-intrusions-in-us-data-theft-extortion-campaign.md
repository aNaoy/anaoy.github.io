---
title: 'UNC3753 Used Vishing and Physical Intrusions in U.S. Data Theft Extortion Campaign'
date: 2026-06-08
permalink: /posts/2026/06/08/unc3753-used-vishing-and-physical-intrusions-in-us-data-theft-extortion-campaign/
tags:
- veille-cyber
- hackernews
---
### Campagne d'extorsion UNC3753 : Vishing et intrusions physiques

Le groupe de menace **UNC3753** (également connu sous les noms de *Chatty Spider*, *Luna Moth* ou *Silent Ransom Group*) cible des entreprises américaines, principalement dans les secteurs juridique, financier et des services professionnels, par le biais de campagnes d'extorsion rapide. Issu des restes du cartel *Conti*, ce groupe privilégie désormais le vol de données à des fins de chantage plutôt que le déploiement de ransomwares.

#### Points clés
*   **Mode opératoire :** Utilisation intensive de l'ingénierie sociale via le *vishing* (phishing vocal). Les attaquants se font passer pour le support informatique afin d'inciter les employés à partager leur écran ou à installer des outils d'accès à distance légitimes.
*   **Escalade physique :** Dans certains cas, les attaquants se présentent physiquement dans les locaux des victimes sous couvert de techniciens IT pour exfiltrer des données via des supports USB.
*   **Rapidité d'exécution :** L'ensemble du cycle, du contact initial à l'exfiltration et à la demande de rançon, peut se dérouler en une seule journée ouvrée.
*   **Infrastructure résiliente :** Le groupe utilise des réseaux de type *DNS Fast Flux* s'appuyant sur des adresses IP résidentielles et mobiles pour rendre leur infrastructure difficile à bloquer.
*   **Cibles privilégiées :** Cabinets juridiques en raison de la nature ultra-confidentielle de leurs données (accords, fusions-acquisitions, données PII).

#### Vulnérabilités exploitées
Cette menace ne repose pas sur une faille technique (CVE) spécifique, mais sur l'exploitation de **vulnérabilités humaines et organisationnelles** :
*   **Contournement des défenses périmétriques :** Le recours à des outils de prise en main à distance légitimes (AnyDesk, Zoom, Microsoft Teams, Zoho Assist) permet de passer outre les solutions de sécurité traditionnelles et l'authentification multifacteur (MFA).

#### Recommandations
*   **Renforcer la sensibilisation :** Former le personnel à la méfiance vis-à-vis des appels téléphoniques non sollicités, même si l'interlocuteur prétend provenir du support informatique interne.
*   **Politique stricte sur les outils distants :** Restreindre l'installation et l'usage de logiciels de contrôle à distance (RMM) sur les postes de travail et surveiller activement leur exécution.
*   **Sécurisation des accès physiques :** Implémenter des protocoles de vérification d'identité stricts pour tout personnel technique externe intervenant sur site.
*   **Gestion des emails :** Sensibiliser les utilisateurs aux tactiques de "préchauffage" par email (emails d'invoices génériques sans lien) servant uniquement à établir un climat de confiance avant l'appel téléphonique.
*   **Surveillance réseau :** Déployer des solutions capables de détecter les anomalies liées à l'utilisation de domaines éphémères et de trafic *Fast Flux*.

---
[Source](https://thehackernews.com/2026/06/unc3753-used-vishing-and-physical.html){:target="_blank"}
