---
title: 'SSL.com rotates their root certificate today, (Tue, May 5th)'
date: 2026-05-05
permalink: /posts/2026/05/05/sslcom-rotates-their-root-certificate-today-tue-may-5th/
tags:
- veille-cyber
- sans-isc
---
### Rotation du certificat racine de SSL.com

SSL.com procède à la rotation de son certificat racine le 5 mai 2026. Bien qu'il s'agisse d'une procédure de maintenance standard pour une autorité de certification (AC), cette mise à jour peut impacter les infrastructures utilisant des configurations spécifiques au-delà du simple chiffrement HTTPS classique.

**Points clés :**
* La transition nécessite une vérification des environnements où les certificats racine sont explicitement configurés ou restreints.
* Les navigateurs et serveurs standards ne devraient pas être affectés, mais les systèmes personnalisés sont à risque de rupture de service.

**Vulnérabilités :**
* Aucune CVE associée (procédure opérationnelle standard). Toutefois, une mauvaise gestion de cette transition peut mener à des erreurs de validation de chaîne de confiance, rendant les services inaccessibles ou vulnérables à des attaques de type « man-in-the-middle » si les certificats sont mal configurés.

**Recommandations :**
* **Audit des configurations :** Examiner les ancres de confiance épinglées (*pinned trust anchors*), les magasins de certificats personnalisés et toute logique de validation liée à l'ancienne hiérarchie de 2016.
* **Continuité :** Utiliser des certificats croisés (*cross-certificates*) pour assurer la rétrocompatibilité durant la phase de transition.
* **Migration :** Privilégier des certificats clients dédiés plutôt que des certificats TLS/SSL polyvalents pour l'authentification, afin de se conformer aux nouvelles exigences des navigateurs (notamment Chrome) concernant l'utilisation des extensions EKU (*Extended Key Usage*).

---
[Source](https://isc.sans.edu/diary/rss/32956){:target="_blank"}
