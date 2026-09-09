---
title: 'Microsoft Plugs Nearly 1,000 Security Holes'
date: 2026-09-09
permalink: /posts/2026/09/09/microsoft-plugs-nearly-1000-security-holes/
tags:
- veille-cyber
- krebs
---
### Record de correctifs chez Microsoft : une gestion des vulnérabilités sous tension

Microsoft a déployé une mise à jour massive corrigeant 974 failles de sécurité, marquant un record historique. Cette augmentation, largement attribuée à l'utilisation de l'intelligence artificielle pour la détection des vulnérabilités, place les équipes informatiques sous une pression opérationnelle inédite pour tester et déployer ces correctifs.

**Points clés :**
* **Volume record :** Plus de 2 600 vulnérabilités corrigées depuis début 2026, soit le double du record de 2020.
* **Complexité accrue :** 113 vulnérabilités sont classées comme « critiques ».
* **Défis opérationnels :** La cadence élevée complique les tests de compatibilité logicielle en entreprise. Les experts recommandent une priorisation basée sur le risque réel plutôt que sur le volume brut de correctifs.

**Vulnérabilités critiques et exploitées (CVE) :**
* **Exploitées activement (Zero-day) :**
    * **CVE-2026-81963** & **CVE-2026-85880** : Permettent une élévation de privilèges sur les systèmes Windows.
* **Vulnérabilités critiques notables :**
    * **CVE-2026-69730 :** Faille DNS affectant Windows Server 2012+ et Windows 10. Risque élevé d'exploitation par l'envoi de paquets malveillants.
    * **CVE-2026-69829 :** Exécution de code à distance (RCE) dans le Shell Windows (Score CVSS : 9.8). Exploitation simplifiée sans interaction utilisateur ni privilèges requis.

**Recommandations :**
* **Pour les entreprises :** Mettre en place une stratégie de priorisation basée sur l'exposition réelle des systèmes. Effectuer des tests rigoureux avant le déploiement général pour éviter les ruptures de service liées aux logiciels tiers.
* **Pour les administrateurs :** Surveiller les ressources spécialisées (comme *AskWoody* ou le *SANS Internet Storm Center*) pour identifier les correctifs problématiques avant déploiement.
* **Pour les utilisateurs particuliers :** Appliquer les mises à jour régulièrement via Windows Update sans attendre, afin d'éviter l'accumulation de failles critiques non résolues.

---
[Source](https://krebsonsecurity.com/2026/09/microsoft-plugs-nearly-1000-security-holes/){:target="_blank"}
