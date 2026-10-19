---
title: 'Unpatched Broadcom Wi-Fi Flaw Lets Attackers in Range Run Code as Root on Routers'
date: 2026-10-19
permalink: /posts/2026/10/19/unpatched-broadcom-wi-fi-flaw-lets-attackers-in-range-run-code-as-root-on-routers/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique dans le logiciel WPS de Broadcom : Risque d'exécution de code à distance

Une faille de sécurité majeure a été découverte dans l'implémentation du protocole Wi-Fi Protected Setup (WPS) intégrée aux puces Broadcom. Cette vulnérabilité permet à un attaquant situé à portée radio de compromettre un routeur sans authentification, de récupérer le mot de passe Wi-Fi ou d'exécuter du code arbitraire avec les privilèges « root ».

**Points clés :**
*   **Vecteur d'attaque :** L'exploitation s'effectue via des messages WPS fragmentés malveillants envoyés par Wi-Fi, provoquant une corruption de la mémoire.
*   **Impact :** Des millions de routeurs et points d'accès à travers le monde sont potentiellement affectés. Sur certains modèles, l'attaque permet d'ouvrir un shell distant (reverse shell) sans nécessiter de serveur externe.
*   **Absence de correctif :** Bien que Broadcom soit informé de ce problème depuis 2018, aucun correctif global n'a été déployé. Pour les anciens modèles (famille eCos), il s'agit d'une vulnérabilité dite « forever day », car aucune mise à jour n'est prévue.
*   **Absence de CVE :** Aucun identifiant CVE n'a été attribué, Broadcom refusant de l'enregistrer officiellement, ce qui a freiné la sensibilisation des fabricants et la distribution de correctifs.

**Vulnérabilités identifiées :**
*   Pas de CVE assigné.
*   Concerne les puces Broadcom (familles eCos : BCM3380/3383/33834 et Linux : BCM3390/65xx/68xx).

**Recommandations :**
*   **Évaluation :** Utiliser les outils fournis par le chercheur (règles YARA pour l'analyse de firmware et scripts de détection en temps réel) disponibles sur son [dépôt GitHub](https://github.com/qkaiser/broadcom-wps) pour identifier les équipements vulnérables.
*   **Atténuation :** Étant donné l'absence de correctif logiciel, la seule solution efficace pour les appareils non supportés ou obsolètes reste le remplacement du matériel.
*   **Vigilance :** Cette faille est particulièrement adaptée aux attaques de proximité (voisinage), une technique déjà utilisée par des groupes de menace avancés pour infiltrer des réseaux ciblés.

---
[Source](https://thehackernews.com/2026/10/unpatched-broadcom-wi-fi-flaw-lets.html){:target="_blank"}
