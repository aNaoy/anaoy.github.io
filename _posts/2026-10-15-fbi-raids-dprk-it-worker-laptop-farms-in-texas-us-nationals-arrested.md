---
title: 'FBI raids DPRK IT worker laptop farms in Texas, US nationals arrested'
date: 2026-10-15
permalink: /posts/2026/10/15/fbi-raids-dprk-it-worker-laptop-farms-in-texas-us-nationals-arrested/
tags:
- veille-cyber
- bleepingcomp
---
### Démantèlement d'un réseau de fermes de serveurs nord-coréennes aux États-Unis

Le département de la Justice des États-Unis (DoJ) a récemment démantelé une opération du groupe de menace nord-coréen *Famous Chollima* (alias *WageMole*). Cette cellule infiltrait des entreprises occidentales en utilisant des travailleurs IT frauduleux pour générer des revenus destinés au régime nord-coréen. Lors de l'opération « Lonestar Roundup » au Texas, le FBI a saisi 187 ordinateurs portables et interpellé des complices américains facilitant cette fraude.

**Points clés :**
* **Modus Operandi :** Des travailleurs nord-coréens se font embaucher à distance en utilisant des identités usurpées. Ils envoient les ordinateurs fournis par les entreprises vers des « fermes » situées aux États-Unis, gérées par des complices locaux, pour simuler une présence physique sur le territoire américain.
* **Impact :** Plus de 70 entreprises américaines ont été impactées, générant environ 3 millions de dollars de profits illicites pour le régime nord-coréen.
* **Techniques de détournement :** Pour acheminer le matériel informatique vers les fermes, les attaquants utilisent de faux rapports de vol, des changements d'adresse de dernière minute ou abusent de leurs privilèges administratifs s'ils occupent des rôles de gestion IT au sein de l'entreprise cible.
* **Actions judiciaires :** 14 personnes ont été inculpées, dont deux ressortissants américains arrêtés pour fraude électronique, blanchiment d'argent et usurpation d'identité.

**Vulnérabilités :**
L'article ne mentionne pas de CVE spécifique, mais met en exergue des vulnérabilités organisationnelles et liées aux processus de recrutement :
* **Processus de vérification d'identité :** Failles dans la validation des antécédents des candidats distants.
* **Gestion des actifs matériels :** Défaut de contrôle sur l'acheminement et la localisation physique du matériel informatique fourni aux employés distants.

**Recommandations :**
* **Vérification accrue :** Renforcer les procédures de vérification d'identité (KYC - Know Your Candidate) lors des recrutements, notamment pour les postes IT à distance.
* **Surveillance des accès :** Implémenter des contrôles stricts sur les accès aux réseaux d'entreprise et surveiller l'utilisation de VPN ou de proxys inhabituels par les employés.
* **Gestion des équipements :** Mettre en place un suivi logistique rigoureux des ordinateurs fournis par l'entreprise et limiter la capacité des employés à détourner les expéditions de matériel.
* **Analyse comportementale :** Surveiller les anomalies dans le comportement des administrateurs IT, particulièrement concernant la gestion des adresses d'expédition et la configuration des accès distants.

---
[Source](https://www.bleepingcomputer.com/news/security/fbi-raids-dprk-it-worker-laptop-farms-in-texas-us-nationals-arrested/){:target="_blank"}
