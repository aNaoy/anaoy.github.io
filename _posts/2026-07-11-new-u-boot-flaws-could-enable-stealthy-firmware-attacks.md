---
title: 'New U-Boot flaws could enable stealthy firmware attacks'
date: 2026-07-11
permalink: /posts/2026/07/11/new-u-boot-flaws-could-enable-stealthy-firmware-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilités critiques dans le chargeur de démarrage U-Boot

Six vulnérabilités ont été découvertes dans le code de vérification de signature FIT (*Flattened Image Tree*) du chargeur de démarrage open-source U-Boot. Ces failles permettent à un attaquant d'exécuter du code arbitraire ou de provoquer un déni de service (DoS) lors du processus de démarrage, avant même le chargement du système d'exploitation.

**Points clés :**
* **Portée étendue :** U-Boot est omniprésent dans les équipements industriels, les serveurs (BMCs), l'IoT et les périphériques réseau. Plus de 50 versions stables sont potentiellement impactées depuis 2013.
* **Persistance furtive :** L'exécution de code au stade du démarrage permet de contourner les protections de sécurité du système d'exploitation, rendant l'installation de malwares difficile à détecter.
* **Vecteur d'attaque :** L'exploitation peut se faire à distance, notamment via des interfaces de gestion (BMCs) supportant les mises à jour de firmware, sans nécessiter d'accès physique.

**Vulnérabilités identifiées :**
Les failles, suivies sous les identifiants Binarly **BRLY-2026-037 à 042**, incluent :
* **Exécution de code arbitraire :** BRLY-2026-037 et BRLY-2026-038 (corruption mémoire).
* **Déni de service (Crash du bootloader) :** BRLY-2026-039 (lecture hors limites), BRLY-2026-040 (déréférencement de pointeur nul), BRLY-2026-041 (validation incorrecte) et BRLY-2026-042 (récursion illimitée).

**Recommandations :**
* **Application des correctifs :** Bien que les correctifs soient intégrés dans le code source amont d'U-Boot, les utilisateurs dépendent de la réactivité des constructeurs (OEM) pour diffuser les mises à jour de firmware.
* **Surveillance du cycle de vie :** Les équipements anciens ou dont le support est terminé ne recevront probablement aucun correctif, les rendant vulnérables de manière permanente. Il est conseillé de segmenter ces dispositifs critiques et de restreindre l'accès aux interfaces de gestion.

---
[Source](https://www.bleepingcomputer.com/news/security/new-u-boot-flaws-could-enable-stealthy-firmware-attacks/){:target="_blank"}
