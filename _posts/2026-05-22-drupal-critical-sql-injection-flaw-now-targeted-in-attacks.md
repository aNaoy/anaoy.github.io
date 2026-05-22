---
title: 'Drupal: Critical SQL injection flaw now targeted in attacks'
date: 2026-05-22
permalink: /posts/2026/05/22/drupal-critical-sql-injection-flaw-now-targeted-in-attacks/
tags:
- veille-cyber
- bleepingcomp
---
# Exploitation active d'une vulnérabilité SQL critique dans Drupal

Drupal a confirmé que des attaquants exploitent activement une vulnérabilité critique d'injection SQL découverte dans son API d'abstraction de base de données. Bien que la faille cible spécifiquement les sites utilisant PostgreSQL, la mise à jour est indispensable pour tous les utilisateurs.

**Points clés :**
* **Nature de la menace :** Injection SQL permettant l'accès non autorisé, la modification ou la suppression de données.
* **Risques associés :** Exécution de code à distance (RCE), élévation de privilèges et divulgation d'informations.
* **Exploitabilité :** La faille est exploitable sans authentification préalable.
* **Contexte :** Drupal a classé le risque comme « hautement critique » (23/25), malgré une évaluation de sévérité moyenne (6.5) par le NIST.

**Vulnérabilité :**
* **CVE-2026-9082 :** Vulnérabilité d'injection SQL affectant l'API d'abstraction de base de données de Drupal.

**Recommandations :**
* **Mise à jour immédiate :** Appliquer les correctifs vers les versions les plus récentes pour chaque branche (10.4.x, 10.5.x, 10.6.x, 11.0.x/11.1.x, 11.2.x, 11.3.x).
* **Considérations pour tous les utilisateurs :** Même les sites n'utilisant pas PostgreSQL doivent mettre à jour leur système, car les correctifs incluent également des mises à jour de sécurité critiques pour les dépendances amont (Symfony et Twig).
* **Fin de support :** Les utilisateurs de Drupal 8 et 9 sont fortement encouragés à migrer, ces versions étant en fin de vie (EoL) et exposées à de multiples vulnérabilités non corrigées.

---
[Source](https://www.bleepingcomputer.com/news/security/drupal-critical-sql-injection-flaw-now-targeted-in-attacks/){:target="_blank"}
