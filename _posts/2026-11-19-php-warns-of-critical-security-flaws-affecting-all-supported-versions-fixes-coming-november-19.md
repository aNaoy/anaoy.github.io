---
title: 'PHP Warns of Critical Security Flaws Affecting All Supported Versions, Fixes Coming November 19'
date: 2026-11-19
permalink: /posts/2026/11/19/php-warns-of-critical-security-flaws-affecting-all-supported-versions-fixes-coming-november-19/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans PHP : correctifs attendus le 19 novembre

L'équipe de maintenance de PHP a annoncé la publication imminente de correctifs de sécurité pour toutes les versions supportées, incluant des vulnérabilités classées comme critiques. Bien que ces failles nécessitent généralement des configurations spécifiques ou peu communes pour être exploitées, leur dangerosité impose une vigilance accrue.

**Points clés :**
*   Une mise à jour corrective majeure est prévue le 19 novembre 2026.
*   Le contexte fait suite à une série de vulnérabilités critiques découvertes récemment, dont celles liées à « PHP2Shell » (CVE-2026-109618 et CVE-2026-109619), activement exploitées sur des infrastructures critiques comme les pare-feu Palo Alto Networks et Check Point.
*   Un autre problème de sécurité majeur (CVE-2026-111497) affectant la bibliothèque Brotli a également été identifié précédemment.

**Vulnérabilités identifiées :**
*   **CVE-2026-115560 :** Une faille d'exécution de code à distance (RCE). L'exploitation réussit si `session.upload_progress.enabled` est activé (paramètre par défaut) et si la configuration de l'application manipule les gestionnaires de session via `ini_set()` vers `php` avant `session_start()`.

**Recommandations :**
*   Appliquer les correctifs officiels dès leur disponibilité le 19 novembre 2026.
*   Pour atténuer temporairement la faille CVE-2026-115560, désactiver la progression de l'upload en configurant `session.upload_progress.enabled=0` dans vos paramètres PHP, puis redémarrer les processus PHP (PHP-FPM/worker).

---
[Source](https://thehackernews.com/2026/11/php-warns-of-critical-security-flaws.html){:target="_blank"}
