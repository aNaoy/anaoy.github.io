---
title: 'BiDi Swap: The bidirectional text trick that makes fake URLs look real'
date: 2025-10-28
permalink: /posts/2025/10/28/bidi-swap-the-bidirectional-text-trick-that-makes-fake-urls-look-real/
tags:
- veille-cyber
- bleepingcomp
---
### Le Piège du BiDi Swap : Quand les Fausses Adresses Deviennent Réelles

Une vulnérabilité ancienne, surnommée BiDi Swap, permet aux cybercriminels de créer des adresses web trompeuses en exploitant la manière dont les navigateurs gèrent les écritures de gauche à droite (LTR) et de droite à gauche (RTL). Cette technique peut être utilisée pour des attaques de phishing, rendant des URL malveillantes indiscernables de liens légitimes.

L'exploitation repose sur le mécanisme de l'algorithme bidirectionnel (Bidi) de Unicode, conçu pour afficher correctement les textes mixtes. Cependant, cet algorithme peut être déjoué au niveau des sous-domaines et des paramètres d'URL, permettant de masquer des caractères trompeurs ou de réorganiser la structure pour faire apparaître une adresse anodine. Des techniques antérieures comme les attaques homographes (utilisant des caractères visuellement similaires mais différents) et les "RTL Override Exploits" ont pavé la voie à cette méthode.

Les navigateurs ont mis en place des protections, mais leur efficacité varie :
*   **Chrome** offre des suggestions pour les URL similaires, mais elle ne couvre pas tous les cas.
*   **Firefox** met en évidence les parties clés du domaine pour aider à repérer les faux liens.
*   **Edge** a indiqué avoir résolu le problème, mais l'affichage de l'URL ne semble pas avoir été modifié.
*   **Arc** (qui n'est plus développé) est cité comme un exemple de navigateur ayant bien implémenté une solution.

**Points Clés :**

*   **Technique :** BiDi Swap, exploitant les spécificités de l'algorithme Bidi de Unicode pour brouiller l'apparence des URL.
*   **Objectif :** Tromper les utilisateurs et les faire atterrir sur des sites malveillants, souvent dans le cadre de campagnes de phishing.
*   **Exploitation :** Manipulation des sous-domaines et des paramètres d'URL en mélangeant des scripts LTR et RTL.

**Vulnérabilités :**

*   Aucune référence CVE spécifique n'est fournie dans l'article, mais il s'agit d'une vulnérabilité comportementale liée à l'implémentation de l'algorithme Bidi dans les navigateurs.

**Recommandations :**

*   **Sensibilisation :** Toujours vérifier la légitimité des URL, surtout celles présentant des motifs inhabituels ou des mélanges de scripts.
*   **Amélioration des navigateurs :** Les développeurs doivent renforcer les protections existantes, comme la mise en évidence des domaines ou la détection d'URL trompeuses.
*   **Éducation :** Inciter les utilisateurs à survoler les liens pour vérifier leur destination, confirmer les certificats SSL et s'assurer de la cohérence du domaine avant de cliquer.

---
[Source](https://www.bleepingcomputer.com/news/security/bidi-swap-the-bidirectional-text-trick-that-makes-fake-urls-look-real/){:target="_blank"}
