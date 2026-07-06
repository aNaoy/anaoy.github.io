---
title: 'New TrojPix Attack Leaks Data From Air-Gapped Systems via Video Cable Emissions'
date: 2026-07-06
permalink: /posts/2026/07/06/new-trojpix-attack-leaks-data-from-air-gapped-systems-via-video-cable-emissions/
tags:
- veille-cyber
- hackernews
---
### TrojPix : Exfiltration de données via les émissions électromagnétiques des câbles vidéo

La technique « TrojPix » permet d'extraire des données de systèmes isolés (air-gapped) en manipulant les pixels affichés à l'écran. Ces modifications, imperceptibles à l'œil humain, transforment le câble vidéo du moniteur en une antenne émettrice radio, permettant à un récepteur à proximité de capter et décoder les informations transmises.

**Points clés :**
*   **Vitesse de transmission :** TrojPix atteint un débit impressionnant de 8,1 Mbps, permettant l'exfiltration de fichiers volumineux en quelques minutes.
*   **Portée :** Des tests ont démontré une portée atteignant jusqu'à 208 mètres dans des conditions optimales.
*   **Discrétion :** L'attaque peut dissimuler le signal soit en faisant apparaître l'écran comme éteint (écran noir), soit en intégrant les données dans le contenu visuel affiché.
*   **Accessibilité :** Ne nécessite pas de droits administrateur ni de modification matérielle ; une simple application malveillante capable d'afficher des images suffit.
*   **Compatibilité :** La méthode a été validée sur une large gamme de moniteurs (9 marques) et de câbles (15 types).

**Vulnérabilités :**
*   Il ne s'agit pas d'une vulnérabilité logicielle classique avec une CVE dédiée, mais d'une exploitation des **émissions électromagnétiques compromettantes (TEMPEST)** inhérentes à l'utilisation de câbles en cuivre pour la transmission de signaux vidéo.

**Recommandations :**
*   **Protection matérielle :** Privilégier l'utilisation de liaisons par fibre optique, qui n'émettent pas de signaux électromagnétiques exploitables.
*   **Blindage physique :** Utiliser des câbles blindés ou opérer dans des environnements sécurisés conformes aux normes TEMPEST (cages de Faraday).
*   **Sécurité préventive :** Puisque TrojPix nécessite une intrusion préalable, le renforcement de la sécurité des points terminaux (EDR, contrôle des accès, restriction des supports USB) reste la défense primaire pour empêcher l'installation initiale du logiciel malveillant.

---
[Source](https://thehackernews.com/2026/07/new-trojpix-attack-leaks-data-from-air.html){:target="_blank"}
