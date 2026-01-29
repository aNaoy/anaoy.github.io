---
title: 'Cyberattack on Polish energy grid impacted around 30 facilities'
date: 2026-01-29
permalink: /posts/2026/01/29/cyberattack-on-polish-energy-grid-impacted-around-30-facilities/
tags:
- veille-cyber
- bleepingcomp
---
### Cyberattaque sur le réseau énergétique polonais : des systèmes critiques ciblés

Fin décembre, une attaque coordonnée a frappé environ 30 sites de production d'énergie décentralisée en Pologne, incluant des installations de cogénération, des parcs éoliens et des systèmes de dispatching solaire. Bien que des équipements opérationnels (OT) aient été endommagés au point d'être irréparables, l'attaque n'a pas entraîné de coupure de courant généralisée.

Une analyse par la société Dragos suggère une forte probabilité que le groupe de menace russe "Electrum", distinct mais potentiellement lié à "Sandworm" (APT44), soit à l'origine de l'attaque. Ce dernier est connu pour avoir utilisé des malwares destructeurs tels que DynoWiper, Caddywiper et Industroyer2 contre des réseaux en Ukraine, notamment dans le secteur de l'énergie.

L'attaquant a démontré une connaissance approfondie des systèmes ciblés, compromettant des unités terminaux distants (RTU), des équipements réseau périphériques, des systèmes de surveillance et de contrôle, ainsi que des machines Windows sur les sites de production d'énergie décentralisée. Ces actions ont entraîné une perte de contrôle et de surveillance à distance, et ont entraîné l'effacement de données sur les systèmes Windows.

Bien que cette attaque n'ait pas causé de panne de courant à l'échelle nationale, elle a mis en évidence la vulnérabilité des systèmes énergétiques décentralisés et aurait pu, si elle avait réussi à interrompre la production, provoquer des déstabilisations du réseau susceptibles de déclencher des défaillances en cascade, comme l'a démontré l'incident de 2025 sur le réseau ibérique.

**Points clés :**

*   Attaque coordonnée visant des sites de production d'énergie décentralisée en Pologne.
*   Dommages matériels sur des équipements critiques (OT) mais pas de coupure de courant généralisée.
*   Implication probable du groupe "Electrum" (potentiellement lié à "Sandworm" / APT44).
*   Démonstration d'une connaissance technique avancée des systèmes industriels par l'attaquant.
*   Mise en évidence de la fragilité des systèmes énergétiques décentralisés et des risques de déstabilisation du réseau.

**Vulnérabilités :**

*   Absence de mesures de sécurité robustes sur les systèmes opérationnels (OT) et de contrôle industriel (ICS).
*   Configurations potentiellement faibles ou erronées des équipements réseau périphériques et des RTU.
*   Exposition des systèmes utilisés pour la communication avec le réseau et le dispatching.

**Recommandations (implicites) :**

*   Renforcer la sécurité des systèmes opérationnels (OT) et des systèmes de contrôle industriel (ICS) par des mesures de protection adaptées.
*   Auditer et sécuriser les configurations des équipements réseau périphériques et des RTU.
*   Segmenter les réseaux et mettre en place une surveillance continue des activités suspectes.
*   Mettre à jour et patcher régulièrement les systèmes d'exploitation et les logiciels utilisés sur les infrastructures critiques.

---
[Source](https://www.bleepingcomputer.com/news/security/cyberattack-on-polish-energy-grid-impacted-around-30-facilities/){:target="_blank"}
