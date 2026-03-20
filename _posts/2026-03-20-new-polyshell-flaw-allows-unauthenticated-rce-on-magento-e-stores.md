---
title: 'New ‘PolyShell’ flaw allows unauthenticated RCE on Magento e-stores'
date: 2026-03-20
permalink: /posts/2026/03/20/new-polyshell-flaw-allows-unauthenticated-rce-on-magento-e-stores/
tags:
- veille-cyber
- bleepingcomp
---
### La faille « PolyShell » : menace critique sur Magento

Une vulnérabilité nommée « PolyShell » affecte l'ensemble des versions stables de Magento Open Source et Adobe Commerce. Elle permet à un attaquant non authentifié d'exécuter du code à distance (RCE) ou de prendre le contrôle de comptes via des attaques XSS (Cross-Site Scripting). Bien qu'aucune exploitation massive n'ait encore été observée, les méthodes d'attaque circulent activement et des offensives automatisées sont imminentes.

**Points clés :**
* **Mécanisme :** La faille réside dans l'API REST de Magento, qui accepte des téléchargements de fichiers via les options personnalisées des articles du panier.
* **Le vecteur d'attaque :** L'utilisation de fichiers « polyglottes » capables de se faire passer pour des images tout en étant interprétés comme des scripts côté serveur.
* **Disponibilité du correctif :** Adobe n'a publié aucun correctif pour les versions en production (actuellement limité à une version alpha 2.4.9), laissant les sites vulnérables.

**Vulnérabilités :**
* **Type :** Téléchargement de fichiers non sécurisé permettant une exécution de code à distance (RCE) et des attaques XSS stockées.
* **CVE :** Aucune CVE n'a été officiellement attribuée à ce jour.

**Recommandations :**
* **Restreindre l'accès :** Bloquer les accès directs au répertoire `pub/media/custom_options/` via les configurations de votre serveur Web (Nginx ou Apache).
* **Audit de sécurité :** Scanner régulièrement le serveur pour détecter la présence de shells, de portes dérobées (backdoors) ou de tout fichier malveillant.
* **Vérification serveur :** S'assurer que les règles de votre hébergeur empêchent réellement l'exécution de scripts dans les dossiers de téléchargement.

---
[Source](https://www.bleepingcomputer.com/news/security/new-polyshell-flaw-allows-unauthenticated-rce-on-magento-e-stores/){:target="_blank"}
