---
title: 'Unpatched Calix flaw lets hackers bypass NAT to expose internal devices'
date: 2026-08-25
permalink: /posts/2026/08/25/unpatched-calix-flaw-lets-hackers-bypass-nat-to-expose-internal-devices/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilité critique sur les routeurs Calix : exposition des réseaux locaux

Une faille de sécurité majeure affecte les routeurs résidentiels Calix GS7 XGS (modèle GS5239XG) utilisant le firmware EXOS version 6.6.47. Cette vulnérabilité permet à tout attaquant distant, sans aucune authentification, de contourner les protections NAT et le pare-feu du routeur pour exposer des appareils internes (caméras, NAS, interfaces d'administration, objets connectés) directement sur Internet.

**Points clés :**
*   **Mécanisme :** Le service UPnP (MiniUPnPd) est exposé sur l'interface WAN via le port TCP 5000 sans aucun contrôle d'accès.
*   **Impact :** Un attaquant peut créer, supprimer ou énumérer des règles de transfert de ports à distance. Les règles créées persistent même après le redémarrage de l'appareil.
*   **État :** Aucune mise à jour corrective n'est disponible à ce jour.

**Vulnérabilité identifiée :**
*   **CVE-2026-75501 :** Défaut d'authentification lié à l'exposition du service SOAP `WANIPConnection` sur l'interface publique.

**Recommandations :**
*   **Désactivation manuelle :** Il est fortement conseillé de désactiver le protocole UPnP via l'interface d'administration du routeur (chemin : *Advanced → Security → UPnP*).
*   **Support FAI :** Si l'option est verrouillée par le fournisseur d'accès, contactez votre opérateur pour demander la désactivation du service UPnP sur votre équipement.
*   **Gestion des ports :** En cas de besoin pour des jeux en ligne ou des applications spécifiques, privilégiez l'ouverture manuelle et ciblée des ports plutôt que d'utiliser UPnP.

---
[Source](https://www.bleepingcomputer.com/news/security/unpatched-calix-flaw-lets-hackers-bypass-nat-to-expose-internal-devices/){:target="_blank"}
