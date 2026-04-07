---
title: 'New GPUBreach Attack Enables Full CPU Privilege Escalation via GDDR6 Bit-Flips'
date: 2026-04-07
permalink: /posts/2026/04/07/new-gpubreach-attack-enables-full-cpu-privilege-escalation-via-gddr6-bit-flips/
tags:
- veille-cyber
- hackernews
---
### GPUBreach : Escalade de privilèges via des failles RowHammer sur GPU

La recherche a mis en évidence une nouvelle classe d'attaques, nommées **GPUBreach**, **GDDRHammer** et **GeForge**, exploitant la technique RowHammer pour provoquer des inversions de bits (bit-flips) dans la mémoire GDDR6 des GPU NVIDIA. Contrairement aux précédentes attaques limitées à la corruption de données, GPUBreach permet une escalade de privilèges complète jusqu'au niveau noyau (root) sur le CPU.

**Points clés :**
* **Contournement de l'IOMMU :** GPUBreach réussit à contourner les protections matérielles de l'IOMMU en corrompant l'état du pilote NVIDIA via des tampons autorisés, déclenchant des écritures hors limites dans le noyau.
* **Impact étendu :** En plus de l'accès arbitraire en lecture/écriture sur la mémoire GPU et CPU, l'attaque peut extraire des clés cryptographiques, altérer la précision de modèles d'IA et ouvrir un interpréteur de commandes (shell) root.
* **Vulnérabilité multi-usage :** Les attaques GDDRHammer et GeForge ciblent également la corruption des tables de pages GPU, offrant des vecteurs d'accès similaires à la mémoire hôte.

**Vulnérabilités :**
* La vulnérabilité réside dans la susceptibilité de la mémoire GDDR6 aux attaques RowHammer.
* L'exploitation repose sur le chaînage de ces inversions de bits avec des bogues de sécurité mémoire présents dans le pilote du noyau NVIDIA. 
* *Note : Aucun identifiant CVE spécifique n'est mentionné dans le texte source.*

**Recommandations :**
* **Activation de l'ECC :** L'activation de la mémoire à code correcteur d'erreurs (ECC) sur les GPU est la mesure d'atténuation temporaire recommandée.
* **Limitations des correctifs :** Les chercheurs soulignent que l'ECC n'est pas une protection infaillible, car des attaques plus sophistiquées peuvent saturer les capacités de correction de l'ECC ou induire des corruptions silencieuses.
* **Absence de protection actuelle :** Pour les GPU grand public (ordinateurs de bureau/portables) ne supportant pas l'ECC, il n'existe actuellement aucune mitigation connue contre ces vecteurs d'attaque.

---
[Source](https://thehackernews.com/2026/04/new-gpubreach-attack-enables-full-cpu.html){:target="_blank"}
