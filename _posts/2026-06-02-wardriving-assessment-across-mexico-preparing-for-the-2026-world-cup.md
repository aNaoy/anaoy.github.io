---
title: 'Wardriving assessment across Mexico: Preparing for the 2026 World Cup'
date: 2026-06-02
permalink: /posts/2026/06/02/wardriving-assessment-across-mexico-preparing-for-the-2026-world-cup/
tags:
- veille-cyber
- securelist
---
### État des lieux de la sécurité Wi-Fi au Mexique : Préparation à la Coupe du Monde 2026

Une évaluation par « wardriving » menée à Mexico, Guadalajara et Monterrey a analysé la sécurité des infrastructures sans fil afin d'anticiper les risques pour les visiteurs internationaux de la Coupe du Monde 2026. L'étude révèle une normalisation excessive des déploiements réseau, augmentant la surface d'attaque globale.

**Points clés :**
*   **Volumétrie :** 84 588 signaux détectés pour 69 473 SSIDs uniques.
*   **Saturation :** Une prévalence massive de la bande 2,4 GHz (95 %) entraîne une forte congestion sur les canaux 1, 6 et 11, nuisant à la stabilité.
*   **Standardisation risquée :** 34 % des réseaux utilisent des noms par défaut (SSID) et de nombreux routeurs conservent des configurations d'usine, facilitant le profilage des infrastructures par les attaquants.
*   **Exposition de métadonnées :** Plus de 30 % des réseaux utilisent leur adresse MAC (BSSID) comme nom de réseau, exposant directement le fabricant du matériel et facilitant la recherche de vulnérabilités spécifiques.
*   **Hétérogénéité sécuritaire :** Bien que 82 % des réseaux utilisent WPA2/WPA3, environ 10 à 12 % restent ouverts et non chiffrés.

**Vulnérabilités identifiées :**
*   **WPS (Wi-Fi Protected Setup) :** 45 % des réseaux analysés ont le WPS activé. Environ la moitié des réseaux sécurisés (WPA2/WPA3) exposent également cette fonction, laquelle est intrinsèquement vulnérable à des attaques par force brute sur le code PIN (ex : vulnérabilités de type *Pixie Dust* ou attaques par dictionnaire liées au protocole WPS).
*   **Profilage par SSID :** L'usage de structures séquentielles ou de noms identifiables (noms de famille, entreprises, adresses) facilite l'ingénierie sociale.
*   **Risques de « Evil Twin » :** La prévisibilité des déploiements simplifie la création de points d'accès malveillants par des attaquants cherchant à intercepter le trafic ou à effectuer des attaques de type *Man-in-the-Middle*.

**Recommandations :**
*   **Désactivation du WPS :** Désactiver systématiquement le WPS sur les routeurs, même si le réseau est chiffré.
*   **Durcissement de la configuration :** Personnaliser le SSID pour supprimer toute référence au fournisseur d'accès (FAI), au modèle du routeur, à l'adresse MAC ou à des informations personnelles.
*   **Migration technologique :** Privilégier le standard WPA3 et migrer vers la bande 5 GHz (ou supérieure) pour réduire la congestion et améliorer la sécurité.
*   **Prudence des utilisateurs :** En zone publique, utiliser systématiquement un VPN, éviter les réseaux ouverts et se méfier des points d'accès ayant des noms génériques ou suspects.

---
[Source](https://securelist.com/wardriving-assessment-in-mexico-fifa-world-cup-2026/119996/){:target="_blank"}
