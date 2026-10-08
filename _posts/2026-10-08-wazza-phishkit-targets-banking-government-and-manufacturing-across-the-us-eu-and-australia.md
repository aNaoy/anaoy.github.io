---
title: 'Wazza Phishkit Targets Banking, Government, and Manufacturing Across the US, EU, and Australia'
date: 2026-10-08
permalink: /posts/2026/10/08/wazza-phishkit-targets-banking-government-and-manufacturing-across-the-us-eu-and-australia/
tags:
- veille-cyber
- hackernews
---
### Analyse de la campagne de phishing Wazza : infrastructure évolutive et évasive

Wazza est un nouveau kit de phishing sophistiqué ciblant les secteurs de la banque, de l'industrie et des institutions gouvernementales aux États-Unis, en Europe et en Australie. Contrairement aux méthodes classiques, Wazza utilise une infrastructure complexe de routage multi-étapes pour filtrer les visiteurs et automatiser le contrôle du trafic avant de présenter une page de phishing usurpant l'identité d'Adobe.

**Points clés :**
* **Mécanisme de filtrage :** L'attaquant utilise des redirections successives pour valider les jetons de session, vérifier la télémétrie du navigateur et filtrer les bots de sécurité.
* **Technique d'hameçonnage :** Utilisation de codes d'appareil (Device Code) Adobe pour contourner les méthodes traditionnelles de récolte de mots de passe et cibler directement l'authentification.
* **Impact opérationnel :** Cette infrastructure rend la détection automatisée difficile et augmente la charge de travail des analystes (notamment pour les MSSP) en masquant le contenu malveillant final derrière une série d'étapes apparemment bénignes.
* **Risques associés :** Compromission de comptes, abus d'identité de confiance au sein des entreprises et facilitation d'attaques de phishing par rebond.

**Vulnérabilités :**
L'article ne mentionne pas de CVE spécifique, car Wazza repose sur des techniques d'ingénierie sociale et d'évasion d'infrastructure plutôt que sur l'exploitation directe de vulnérabilités logicielles identifiées.

**Recommandations :**
* **Utilisation d'environnements isolés (Sandboxing) :** Adopter des solutions interactives pour reproduire la chaîne de routage complète et observer le comportement réel du lien, plutôt que de se fier uniquement à l'analyse statique de l'URL.
* **Approche axée sur le renseignement (Threat Intelligence) :** Ne pas se contenter de bloquer des domaines isolés. Utiliser les indicateurs de compromission (IOC) extraits pour alimenter des flux de renseignements (TI Feeds) permettant une surveillance continue.
* **Automatisation des flux de travail :** Intégrer les outils de sandbox et les flux de renseignements directement dans les systèmes de gestion des incidents (type SIEM/SOAR) pour accélérer le temps de réponse et réduire le besoin d'escalade vers les analystes seniors.
* **Visualisation des menaces :** Analyser les pivots de l'infrastructure (endpoints, chemins de redirection) pour cartographier l'ensemble de la campagne plutôt que de traiter chaque alerte comme un incident isolé.

---
[Source](https://thehackernews.com/2026/10/wazza-phishkit-targets-banking.html){:target="_blank"}
