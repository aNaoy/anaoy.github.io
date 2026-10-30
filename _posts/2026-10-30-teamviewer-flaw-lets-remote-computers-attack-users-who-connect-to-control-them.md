---
title: 'TeamViewer Flaw Lets Remote Computers Attack Users Who Connect to Control Them'
date: 2026-10-30
permalink: /posts/2026/10/30/teamviewer-flaw-lets-remote-computers-attack-users-who-connect-to-control-them/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique dans TeamViewer : Risque d'exécution de code à distance par l'hôte

Une faille de sécurité majeure permet à une machine distante (l'hôte) de compromettre l'ordinateur qui se connecte pour en prendre le contrôle (le client/viewer). L'exploitation survient lors de l'établissement d'une session de contrôle à distance, lorsqu'un hôte malveillant transmet des informations de taille d'écran falsifiées, provoquant un dépassement de tampon (*buffer overflow*) dans le client.

**Points clés :**
* **Mécanisme :** L'attaque exploite une erreur de calcul mémoire côté client lors de la réception des données d'affichage envoyées par l'hôte.
* **Impact :** Provoque systématiquement le crash de l'application cliente et permet, selon la plateforme (notamment sous Windows), l'exécution de code arbitraire sur la machine du viewer.
* **Accessibilité :** L'attaque ne nécessite aucun mot de passe supplémentaire ni interaction spécifique de l'utilisateur, au-delà de l'acceptation de la session distante. Elle est réalisable avec la configuration par défaut de l'application.

**Vulnérabilité identifiée :**
* **CVE-2026-111585** (Score : 8.8/10)
* **Systèmes affectés :** TeamViewer Full Client (Windows, Linux, macOS), version portable pour Windows et l'application Android, pour toutes les versions antérieures à la 15.83.

**Recommandations :**
* **Mise à jour immédiate :** La seule solution est de mettre à jour TeamViewer vers la **version 15.83** ou une version ultérieure.
* **Portée :** La mise à jour est indispensable pour tous les types d'installations, y compris les versions "Host", car elle corrige également d'autres vulnérabilités critiques liées à l'exécution de code à distance.
* **Vigilance :** Bien qu'aucune exploitation massive n'ait été rapportée à ce jour, l'application des correctifs est urgente en raison du score de sévérité élevé.

---
[Source](https://thehackernews.com/2026/10/teamviewer-flaw-lets-remote-computers.html){:target="_blank"}
