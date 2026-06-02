---
title: 'New Wave Of Phishing Emails with SVG Files, (Tue, Jun 2nd)'
date: 2026-06-02
permalink: /posts/2026/06/02/new-wave-of-phishing-emails-with-svg-files-tue-jun-2nd/
tags:
- veille-cyber
- sans-isc
---
### Propagation de campagnes de phishing via des fichiers SVG malveillants

Une nouvelle vague d'emails malveillants utilise des fichiers SVG (Scalable Vector Graphic) comme vecteurs d'attaque. Bien que le format SVG soit normalement destiné aux graphiques, les attaquants y intègrent du code JavaScript pour rediriger les navigateurs des victimes vers des pages de phishing.

**Points clés :**
*   **Technique d'évasion :** Les attaquants utilisent le type MIME `application/ecmascript` au lieu des classiques `text/javascript` ou `application/javascript` pour contourner les outils de sécurité (WAF, filtres) basés sur des signatures de détection.
*   **Obfuscation :** Le script inclus dans le fichier SVG utilise une combinaison de codage Base64 et d'opérations XOR pour masquer l'URL de destination.
*   **Exploitation du système :** La méthode repose sur le fait que les navigateurs sous Windows ouvrent et interprètent nativement les fichiers SVG, exécutant ainsi le script malveillant sans interaction complexe.
*   **TLD douteux :** La campagne privilégie des domaines utilisant le TLD `.cfd` (Clothing, Fashion, and Design), souvent utilisé par des acteurs malveillants en raison de son faible coût.

**Vulnérabilités :**
*   Il ne s'agit pas d'une vulnérabilité logicielle spécifique (CVE), mais d'un abus de la conception par défaut des navigateurs qui traitent et exécutent automatiquement les scripts contenus dans les fichiers SVG.

**Recommandations :**
*   **Filtrage des pièces jointes :** Mettre en place des règles de passerelle de messagerie pour bloquer ou isoler les fichiers `.svg` provenant de sources externes.
*   **Éducation des utilisateurs :** Sensibiliser les employés au risque associé aux fichiers images inhabituels reçus par email.
*   **Analyse EDR/WAF :** Mettre à jour les outils de détection pour inspecter spécifiquement le contenu des fichiers SVG et identifier l'usage de types MIME moins courants ou suspects comme `application/ecmascript`.

---
[Source](https://isc.sans.edu/diary/rss/33040){:target="_blank"}
