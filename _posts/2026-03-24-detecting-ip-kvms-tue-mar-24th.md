---
title: 'Detecting IP KVMs, (Tue, Mar 24th)'
date: 2026-03-24
permalink: /posts/2026/03/24/detecting-ip-kvms-tue-mar-24th/
tags:
- veille-cyber
- sans-isc
---
### Détection et risques liés aux boîtiers IP KVM « pirates »

Les dispositifs IP KVM (Keyboard, Video, Mouse) sont de plus en plus détournés par des acteurs malveillants pour établir des accès distants non autorisés, que ce soit pour usurper une identité professionnelle (télétravail illégitime) ou pour maintenir une persistance sur un réseau après une intrusion physique.

**Points clés :**
* **Usage malveillant :** Ces boîtiers permettent de prendre le contrôle d'un poste de travail à distance de manière furtive, en contournant les politiques de sécurité habituelles.
* **Mécanismes de connexion :** Les dispositifs se connectent via USB (clavier/souris) et HDMI (affichage).
* **Détection technique :** Il est possible d'identifier ces appareils en analysant les identifiants USB (`lsusb`) ou les données EDID (Extended Display Identification Data) transmises par le signal HDMI.
* **Limites de la détection :** La détection est vulnérable au contournement, car des attaquants avertis peuvent modifier manuellement les chaînes d'identification (noms de modèles, fabricants) via les fichiers de configuration du KVM.

**Vulnérabilités :**
* L'article ne mentionne pas de CVE spécifique, mais souligne une faille structurelle : la confiance implicite des systèmes d'exploitation envers les périphériques USB et d'affichage connectés, permettant une intrusion "matérielle" invisible pour la plupart des logiciels de protection.

**Recommandations :**
* **Surveillance des périphériques :** Auditer régulièrement les listes de périphériques connectés (`lsusb`) sur les postes de travail critiques.
* **Analyse EDID :** Intégrer la vérification des données EDID des écrans connectés dans les outils de gestion du parc informatique ou de surveillance. 
* **Politique de sécurité :** Restreindre physiquement l'accès aux ports USB et HDMI sur les postes sensibles et surveiller l'ajout de matériel inconnu.
* **Attention aux alertes :** Considérer tout nouveau périphérique USB ou moniteur dont l'identification semble inhabituelle ou générique comme une menace potentielle, surtout en environnement professionnel.

---
[Source](https://isc.sans.edu/diary/rss/32824){:target="_blank"}
