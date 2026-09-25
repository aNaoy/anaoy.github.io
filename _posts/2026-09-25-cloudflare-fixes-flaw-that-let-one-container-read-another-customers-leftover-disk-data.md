---
title: 'Cloudflare Fixes Flaw That Let One Container Read Another Customers Leftover Disk Data'
date: 2026-09-25
permalink: /posts/2026/09/25/cloudflare-fixes-flaw-that-let-one-container-read-another-customers-leftover-disk-data/
tags:
- veille-cyber
- hackernews
---
### Fuite de données inter-conteneurs chez Cloudflare

Une vulnérabilité majeure a été identifiée au sein de l'infrastructure de stockage partagé de Cloudflare, permettant à un client de consulter des données résiduelles provenant des disques d'autres clients. Ce défaut, lié à une mauvaise configuration du "thin provisioning" sous Linux, permettait de récupérer des blocs de données non effacés après la suppression d'un conteneur.

**Points clés :**
* **Nature de la faille :** Défaut de configuration du *device-mapper* (thin provisioning) omettant l'effacement sécurisé des blocs de stockage avant leur réallocation.
* **Impact :** Récupération possible de fichiers sensibles (bases de données SQLite, profils de navigation, fichiers `.env`, identifiants) présents dans les blocs réutilisés.
* **Portée :** Affectait les services Cloudflare Containers et Cloudflare Sandboxes.
* **Aucune exploitation malveillante détectée :** Cloudflare a audité ses logs et n'a trouvé aucune preuve d'exploitation par des tiers, seuls les chercheurs ayant signalé la faille et ses ingénieurs ont effectué des tests.

**Vulnérabilités :**
* Aucune CVE n'a été attribuée publiquement à ce jour, la faille relevant d'une mauvaise configuration de sécurité interne plutôt que d'un bug logiciel spécifique.

**Recommandations :**
* **Pour les utilisateurs :** Aucune action requise. Cloudflare a confirmé avoir réactivé l'effacement automatique des blocs, redémarré les conteneurs et vidé les caches de stockage.
* **Pour les prestataires cloud :** S'assurer que le *thin provisioning* inclut systématiquement une procédure de nettoyage (wiping) des blocs avant toute réattribution à un nouveau client pour garantir l'isolation des données.

---
[Source](https://thehackernews.com/2026/09/cloudflare-fixes-flaw-that-let-one.html){:target="_blank"}
