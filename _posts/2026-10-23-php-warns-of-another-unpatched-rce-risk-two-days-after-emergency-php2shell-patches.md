---
title: 'PHP Warns of Another Unpatched RCE Risk Two Days After Emergency PHP2Shell Patches'
date: 2026-10-23
permalink: /posts/2026/10/23/php-warns-of-another-unpatched-rce-risk-two-days-after-emergency-php2shell-patches/
tags:
- veille-cyber
- hackernews
---
### Nouvelle vulnérabilité RCE identifiée dans PHP

PHP a signalé une nouvelle vulnérabilité permettant potentiellement l'exécution de code à distance (RCE), survenant seulement deux jours après le déploiement de correctifs d'urgence pour les failles critiques « PHP2Shell ».

**Points clés :**
*   **Risque limité :** La vulnérabilité ne concerne que des configurations web très spécifiques et peu courantes.
*   **Absence de correctif immédiat :** PHP ne prévoit pas de mise à jour d'urgence ; la correction sera intégrée au prochain cycle de publication régulier.
*   **Contexte de menaces :** Les tentatives d'exploitation des failles précédentes (PHP2Shell) ont drastiquement augmenté, visant notamment l'installation de botnets comme Mirai, bien qu'aucune exploitation confirmée du nouveau CVE n'ait été rapportée à ce jour.

**Vulnérabilités :**
*   **CVE-2026-115560 :** Nouvelle faille RCE liée à une configuration spécifique de la fonction « session upload progress ».
*   **CVE-2026-109618 & CVE-2026-109619 :** Failles critiques « PHP2Shell » (corrigées le 21 octobre).

**Recommandations :**
*   **Désactivation de la fonctionnalité :** Il est conseillé de désactiver la fonctionnalité de suivi de progression des téléchargements en configurant `session.upload_progress.enabled=0` dans vos paramètres PHP jusqu'à la disponibilité du correctif.
*   **Vérification de configuration :** Cette mesure est particulièrement cruciale pour les applications qui modifient le `session.serialize_handler` via `ini_set()` avant l'appel de `session_start()`. Si cette option a déjà été désactivée suite aux alertes précédentes du 21 octobre, aucune action supplémentaire n'est requise.

---
[Source](https://thehackernews.com/2026/10/urgent-php-warns-of-another-unpatched.html){:target="_blank"}
