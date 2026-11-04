---
title: 'Critical Rails Flaw Lets Attackers Write Server Files via Crafted ImageMagick Uploads'
date: 2026-11-04
permalink: /posts/2026/11/04/critical-rails-flaw-lets-attackers-write-server-files-via-crafted-imagemagick-uploads/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique d'écriture de fichiers dans Ruby on Rails

Une faille de sécurité critique (score CVSS 9.8) dans le module **Active Storage** de Ruby on Rails permet à un attaquant non authentifié d'écrire, et potentiellement de lire, des fichiers arbitraires sur le serveur via le téléchargement d'images malveillantes.

**Points clés :**
* **Mécanisme :** La vulnérabilité exploite la manière dont Active Storage traite les fichiers avec **ImageMagick**. Un fichier SVG spécifiquement conçu peut utiliser le codeur « MSL » (outil de script) d'ImageMagick pour manipuler les fichiers du système.
* **Impact :** Lecture de fichiers sensibles (clés secrètes, identifiants), exécution de code à distance (RCE) et mouvements latéraux au sein des systèmes compromis.
* **Vulnérabilités :**
    * **GHSA-f3w6-w445-fwh9** : Faille principale d'écriture de fichiers arbitraires.
    * **GHSA-v924-7rp8-4mxh** : Faille secondaire permettant à un attaquant de choisir le décodeur utilisé en manipulant l'extension des fichiers.
* **Conditions d'exposition :** L'application est vulnérable si elle utilise ImageMagick pour le traitement d'images (`config.active_storage.variant_processor = :mini_magick`), que sa politique de sécurité ImageMagick est permissive et qu'elle accepte des fichiers provenant d'utilisateurs non fiables.

**Recommandations :**
* **Mise à jour :** Appliquer immédiatement les versions **Rails 8.1.4.1** ou **8.0.5.2**.
* **Configuration :** S'assurer que la gem `mini_magick` est en version 5.1 ou supérieure. Vérifier l'application de la nouvelle politique de sécurité intégrée via la commande : `bin/rails runner 'puts MiniMagick.identify { |i| i.list "policy" }'`.
* **Atténuation manuelle :** Si une mise à jour immédiate est impossible, copier manuellement les règles de la politique de sécurité fournie par Rails (`activestorage/lib/active_storage/image_magick/policy.xml`) dans le fichier système `policy.xml` d'ImageMagick pour bloquer les codeurs MSL et Ghostscript.
* **Audit de sécurité :** En cas d'utilisation du service de stockage disque, considérer que les secrets (`secret_key_base`, identifiants, jetons API) ont pu être compromis et procéder à leur renouvellement immédiat.

---
[Source](https://thehackernews.com/2026/11/critical-rails-flaw-lets-attackers.html){:target="_blank"}
