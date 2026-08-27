---
title: 'New GPUThor Rowhammer Defeats ECC on NVIDIA RTX A6000 to Gain Host Root Access'
date: 2026-08-27
permalink: /posts/2026/08/27/new-gputhor-rowhammer-defeats-ecc-on-nvidia-rtx-a6000-to-gain-host-root-access/
tags:
- veille-cyber
- hackernews
---
### GPUThor : Une nouvelle vulnérabilité Rowhammer contourne l'ECC sur GPU NVIDIA

Des chercheurs de l'Université de Toronto ont dévoilé **GPUThor**, une variante avancée de l'attaque Rowhammer capable de contourner les codes de correction d'erreurs (ECC), la protection principale recommandée par NVIDIA. En exploitant des accès mémoire non uniformes sur les GPU de classe Ampere, cette attaque permet de provoquer des inversions de bits massives, menant à des dénis de service (DoS) ou à une élévation de privilèges (accès root).

#### Points clés
* **Technique :** L'attaque utilise un martelage ("hammering") non uniforme pour saturer les défenses de rafraîchissement des lignes mémoires (TRR), surpassant largement en efficacité les précédentes méthodes comme GPUHammer.
* **Impact de l'ECC :** Bien que l'ECC puisse détecter et corriger certaines erreurs, l'attaque génère des erreurs multiples (doubles ou triples) que l'ECC ne peut pas corriger, provoquant une corruption silencieuse des données (SDC) ou des erreurs irrécupérables (DUE) entraînant le plantage du GPU.
* **Escalade de privilèges :** Les attaquants manipulent les tables de pages (page tables) en corrompant la mémoire, permettant d'écraser les structures d'identification du système et d'obtenir les droits root sur l'hôte.
* **CVE :** Aucune identification CVE n'a été attribuée à cette vulnérabilité à ce jour.

#### Vulnérabilités matérielles
Les tests ont confirmé la vulnérabilité des modèles suivants équipés de mémoire GDDR6 :
* NVIDIA RTX A6000, A5000, A4500 et A4000.
* *Note : Les modèles plus récents, HBM2e, GDDR6X et certaines architectures serveur n'ont pas montré de vulnérabilité lors des tests avec ces modèles spécifiques.*

#### Recommandations
* **Ne pas compter exclusivement sur l'ECC :** Bien que l'ECC reste utile, les chercheurs soulignent qu'il n'est plus suffisant comme défense unique.
* **Isolement :** Éviter le partage de GPU entre différents locataires (multi-tenant) dans des environnements cloud.
* **Gestion des accès :** Restreindre strictement l'exécution de kernels CUDA non approuvés.
* **Surveillance :** Surveiller activement les compteurs d'erreurs ECC pour détecter d'éventuelles tentatives d'attaque en cours.
* **Mise à jour :** Consulter les avis de sécurité officiels de NVIDIA (notamment l'avis de juillet 2026) pour appliquer les conseils de configuration recommandés par le constructeur.

---
[Source](https://thehackernews.com/2026/08/gputhor-rowhammer-defeats-ecc-on-nvidia.html){:target="_blank"}
