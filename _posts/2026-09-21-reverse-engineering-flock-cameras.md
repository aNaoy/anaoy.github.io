---
title: 'Reverse-Engineering Flock Cameras'
date: 2026-09-21
permalink: /posts/2026/09/21/reverse-engineering-flock-cameras/
tags:
- veille-cyber
- schneier
---
### Analyse des failles de sécurité des caméras Flock

L'ingénierie inverse d'une caméra de lecture automatique de plaques d'immatriculation (ALPR) de la société Flock a révélé des capacités de surveillance étendues, allant au-delà de la simple lecture de plaques. Le logiciel intégré détecte et enregistre systématiquement les personnes, les vélos et divers détails graphiques (autocollants, écussons), générant des millions d'images.

**Points clés :**
*   **Capacités de surveillance :** L'appareil effectue une analyse par vision par ordinateur hautement détaillée, capable d'isoler des éléments spécifiques sur des objets ou des individus.
*   **Volume de données :** Une seule caméra peut générer plus d'un million d'images sur une courte période.
*   **Défaut de conception critique :** La sécurité repose sur un chiffrement défaillant, rendant la protection des données quasi inexistante.

**Vulnérabilités :**
*   **Gestion des clés de chiffrement :** La clé de déchiffrement d'une partition sécurisée était stockée en clair sur une partition non chiffrée du même appareil. Aucune CVE n'est associée à cet incident spécifique à ce jour, il s'agit d'une faille de conception architecturale.

**Recommandations :**
*   **Séparation des accès :** Ne jamais stocker de clés de chiffrement sur des supports accessibles ou non chiffrés.
*   **Renforcement du chiffrement :** Utiliser des modules de sécurité matériels (HSM) ou des solutions de gestion de clés distantes pour isoler les secrets de la machine hôte.
*   **Audit de sécurité :** Effectuer des tests d'intrusion rigoureux pour valider l'étanchéité des partitions de données et la robustesse des mécanismes de protection contre l'ingénierie inverse.

---
[Source](https://www.schneier.com/blog/archives/2026/09/reverse-engineering-flock-cameras.html){:target="_blank"}
