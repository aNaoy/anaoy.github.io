---
title: 'PHP ships emergency patches for critical PHP2Shell flaws'
date: 2026-10-21
permalink: /posts/2026/10/21/php-ships-emergency-patches-for-critical-php2shell-flaws/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilités critiques "PHP2Shell" : correctifs d'urgence disponibles

L'équipe de sécurité PHP a publié des correctifs pour deux vulnérabilités critiques de type exécution de code à distance (RCE), regroupées sous le nom de **PHP2Shell**. Ces failles touchent la quasi-totalité des environnements PHP (PHP-FPM, Apache mod_php, php-cgi, etc.) et permettent à un attaquant non authentifié de prendre le contrôle du serveur en exploitant une corruption de la mémoire.

**Points clés :**
*   **Risque majeur :** Le risque est considéré comme maximal pour `mod_php`, car l'attaque peut être déclenchée avant même l'exécution du code applicatif.
*   **État de la menace :** Des attaques actives exploitant ces vulnérabilités ont déjà été observées.
*   **Portée :** Affecte toutes les versions actuelles de PHP ; les versions 8.1 et antérieures, bien que non supportées, ont reçu des correctifs de source pour aider les administrateurs.

**Vulnérabilités :**
*   **CVE-2026-109618 :** Exploite une chaîne de faiblesses déclenchant une corruption mémoire (out-of-memory).
*   **CVE-2026-109619 :** Vulnérabilité liée à l'état global résiduel permettant une corruption de type *use-after-free* sur le tas (heap), une divulgation de mémoire et une RCE.

**Recommandations :**
1.  **Mise à jour immédiate :** Installez les versions corrigées dès que possible : PHP 8.5.12, 8.4.27, 8.3.36 ou 8.2.35.
2.  **Versions obsolètes :** Pour les serveurs utilisant PHP 8.1 ou inférieur, contactez votre fournisseur pour obtenir des correctifs rétroportés (backports) ou migrez vers une version supportée.
3.  **Atténuation temporaire (si le patch est impossible) :**
    *   **Pour CVE-2026-109618 :** Limiter l'usage mémoire avec `memory_limit=-1`, réduire la taille maximale des téléchargements (`post_max_size`), et utiliser des conteneurs pour isoler les travailleurs.
    *   **Pour CVE-2026-109619 :** Désactiver la progression des uploads (`session.upload_progress.enabled=0`), désactiver les traces d'erreurs fatales (`fatal_error_backtraces=0` sur PHP 8.5) et nettoyer les configurations obsolètes. 
    *   *Note : Ces mesures ne constituent pas une protection complète ; seule l'application des correctifs officiels garantit une défense pérenne.*

---
[Source](https://www.bleepingcomputer.com/news/security/php-ships-emergency-patches-for-critical-php2shell-flaws/){:target="_blank"}
