---
title: 'GPS As a Key Distribution Platform'
date: 2026-06-09
permalink: /posts/2026/06/09/gps-as-a-key-distribution-platform/
tags:
- veille-cyber
- schneier
---
### Le GPS détourné en station de radiodiffusion cryptographique

Des recherches suggèrent que l'armée américaine utilise le réseau GPS mondial pour diffuser discrètement des clés de chiffrement depuis près de 20 ans. Cette méthode transforme chaque satellite en une « station de nombres » dissimulée, permettant la mise à jour des dispositifs militaires sans intervention physique.

**Points clés :**
* **Système OTAD/OTAR :** Le déploiement des protocoles *Over-the-Air Distribution* et *Over-the-Air Rekeying* a permis de remplacer la distribution manuelle de matériel cryptographique par une transmission à distance via les satellites GPS.
* **Preuves empiriques :** Une corrélation temporelle a été établie entre les pics de données suspects émis par les 31 satellites opérationnels et le calendrier de déploiement officiel des systèmes de rekeying militaire identifié dans des documents déclassifiés.
* **Portée mondiale :** Tous les appareils compatibles GPS reçoivent techniquement ces transmissions masquées, bien que leur contenu reste chiffré et inaccessible aux utilisateurs civils.

**Vulnérabilités :**
* Aucune CVE n'est associée à cette découverte, car il ne s'agit pas d'une faille logicielle exploitée par des tiers, mais d'une fonctionnalité intégrée au protocole GPS par le gouvernement américain. Toutefois, l'existence d'un canal de communication « caché » dans une infrastructure publique pose des questions sur l'intégrité et la sécurité du signal GPS.

**Recommandations :**
* Bien qu'aucune mesure corrective ne soit possible pour les utilisateurs finaux, les chercheurs en sécurité et les concepteurs de protocoles de géolocalisation doivent être conscients de cette capacité de transmission auxiliaire intégrée, qui pourrait théoriquement être détournée ou utilisée pour des attaques par canal auxiliaire (side-channel) si des vulnérabilités étaient découvertes dans le traitement de ces paquets de données « fantômes » par les récepteurs GPS.

---
[Source](https://www.schneier.com/blog/archives/2026/06/gps-as-a-key-distribution-platform.html){:target="_blank"}
