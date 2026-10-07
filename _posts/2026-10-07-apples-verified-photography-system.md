---
title: 'Apple’s Verified Photography System'
date: 2026-10-07
permalink: /posts/2026/10/07/apples-verified-photography-system/
tags:
- veille-cyber
- schneier
---
### Authentification sécurisée des photos Apple

Apple a lancé « Reference Image », un système permettant de certifier l’authenticité d’une image prise par un iPhone récent sans compromettre l’anonymat du photographe. La solution repose sur une signature numérique délivrée par les serveurs d'Apple après une validation via *Private Cloud Compute* (PCC), garantissant que l'image provient bien d'un capteur matériel authentique.

**Points clés :**
* **Anonymat préservé :** Aucune identification du photographe ou de l'appareil n'est requise pour valider l'authenticité de l'image.
* **Confidentialité des données :** Les pixels des images ne sont jamais exposés à Apple, le traitement étant effectué au sein de l'infrastructure sécurisée PCC.
* **Intégrité matérielle :** Le système permet de vérifier que plusieurs clichés proviennent du même capteur tout en isolant ces données de toute identité publique.
* **Révocation privée :** La vérification de la validité d'une image s'effectue via des listes stockées localement sur l'appareil, empêchant le suivi ou l'identification de l'usage fait par l'utilisateur.

**Vulnérabilités :**
* Aucune vulnérabilité spécifique (CVE) n'est mentionnée dans l'article, le système étant présenté comme une implémentation native visant à renforcer la confiance dans le contenu numérique.

**Recommandations :**
* Privilégier l'utilisation de matériels prenant en charge cette technologie pour les contextes sensibles (journalisme, zones de conflit) afin de garantir l'intégrité des preuves visuelles sans exposer l'identité de l'auteur.

---
[Source](https://www.schneier.com/blog/archives/2026/10/apples-verified-photography-system.html){:target="_blank"}
