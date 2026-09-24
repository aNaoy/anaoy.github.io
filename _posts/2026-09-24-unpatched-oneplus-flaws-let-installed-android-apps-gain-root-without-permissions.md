---
title: 'Unpatched OnePlus Flaws Let Installed Android Apps Gain Root Without Permissions'
date: 2026-09-24
permalink: /posts/2026/09/24/unpatched-oneplus-flaws-let-installed-android-apps-gain-root-without-permissions/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques d'élévation de privilèges sur les appareils OnePlus

Des failles de sécurité non corrigées dans OxygenOS permettent à une application malveillante installée localement d'obtenir un accès root complet, sans aucune autorisation préalable de l'utilisateur.

**Points clés :**
* **Mécanisme d'attaque :** L'exploitation repose sur le chaînage de deux vulnérabilités logicielles. La première permet d'accéder au compte root dans une zone restreinte via le service `AtlasService`. La seconde utilise un service d'assistance matérielle (`olc2`) pour exécuter des commandes shell arbitraires avec des privilèges système totaux.
* **Impact :** Une application malveillante peut prendre le contrôle total du système, y compris charger du code noyau, sans interaction ni permission de l'utilisateur.
* **Portée :** Les modèles récents comme le OnePlus 15 et le OnePlus 12 Pro sont touchés. OnePlus a indiqué que ces failles affectent également une large gamme d'appareils de sa marque ainsi que ceux d'OPPO.
* **Conflit de divulgation :** Le chercheur Rasmus Moorats a rendu les failles publiques après cinq mois d'attente, malgré les menaces de poursuites judiciaires de OnePlus, qui revendique le droit exclusif de divulgation et n'avait fourni aucun correctif.

**Vulnérabilités :**
* Aucune référence CVE n'a été attribuée à ce jour.

**Recommandations :**
* **Prudence lors de l'installation :** En l'absence de correctif, la seule protection efficace est de n'installer que des applications provenant de sources fiables.
* **Vigilance :** L'attaque étant locale, elle nécessite obligatoirement la présence d'un logiciel malveillant sur le terminal. Évitez les applications suspectes ou provenant de boutiques tierces non vérifiées.

---
[Source](https://thehackernews.com/2026/09/unpatched-oneplus-flaws-let-installed.html){:target="_blank"}
