---
title: 'Yandex confirms service outage as users lose access to cloud files'
date: 2026-10-13
permalink: /posts/2026/10/13/yandex-confirms-service-outage-as-users-lose-access-to-cloud-files/
tags:
- veille-cyber
- bleepingcomp
---
### Perturbation majeure des services Cloud de Yandex suite à des attaques physiques

Le fournisseur de services cloud russe Yandex subit une interruption de service prolongée après que trois de ses centres de données (Sasovo, Kaluga et Vladimir) ont été endommagés par des attaques de drones entre le 8 et le 11 octobre 2026. Cette situation a entraîné une indisponibilité totale de deux sites et une dégradation critique du troisième, impactant l'accès aux fichiers, aux bases de données et aux infrastructures de stockage S3.

**Points clés :**
*   **Origine des incidents :** Attaques ciblées par drones, attribuées aux forces ukrainiennes, visant à paralyser l'infrastructure technologique majeure de la Russie.
*   **Impact opérationnel :** Yandex a qualifié sa configuration actuelle de ressources d'« instable » et fonctionne en mode d'urgence. De nombreux services (Compute, API, stockage) connaissent des erreurs HTTP (500, 504, 302).
*   **Incertitude sur les données :** La firme n'a pas confirmé si les données inaccessibles dans les centres détruits sont définitivement perdues.
*   **Vulnérabilités :** Aucune CVE spécifique n'est associée, car il s'agit d'une destruction physique des infrastructures matérielles et non d'une faille logicielle ou réseau.

**Recommandations :**
*   **Recours aux plans de continuité :** Yandex conseille formellement à ses clients de basculer immédiatement vers des infrastructures alternatives de reprise après sinistre (Disaster Recovery).
*   **Diversification :** Ne pas dépendre d'un seul fournisseur cloud pour les données critiques et maintenir des sauvegardes géographiquement isolées du fournisseur principal.
*   **Surveillance :** Maintenir une veille constante sur le tableau de bord d'état des services (*Status Page*) de Yandex, bien que la restauration des services soit actuellement sans calendrier précis.

---
[Source](https://www.bleepingcomputer.com/news/security/yandex-confirms-service-outage-as-users-lose-access-to-cloud-files/){:target="_blank"}
