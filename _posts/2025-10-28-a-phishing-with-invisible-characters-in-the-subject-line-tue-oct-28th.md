---
title: 'A phishing with invisible characters in the subject line, (Tue, Oct 28th)'
date: 2025-10-28
permalink: /posts/2025/10/28/a-phishing-with-invisible-characters-in-the-subject-line-tue-oct-28th/
tags:
- veille-cyber
- sans-isc
---
**Objet de courriel d'hameçonnage contournant les filtres de sécurité**

Une technique d'hameçonnage récente utilise des caractères invisibles, spécifiquement le trait d'union conditionnel (U+00AD), dans la ligne d'objet des courriels pour échapper aux systèmes de détection automatique. Ce caractère, bien que techniquement non invisible, n'est généralement pas rendu par les clients de messagerie comme Outlook.

L'attaquant a encodé la ligne d'objet en utilisant le format MIME "encoded-word" (RFC 2047) avec un encodage UTF-8 et Base64. Le caractère de trait d'union conditionnel a été inséré à plusieurs reprises dans les chaînes de caractères encodées, divisant ainsi l'objet en plusieurs parties. Cette méthode vise à perturber les filtres de sécurité qui analysent les sujets des courriels pour identifier les menaces potentielles.

Cette approche est notable car elle est appliquée spécifiquement à la ligne d'objet, alors que l'utilisation de caractères invisibles est plus courante dans le corps des messages pour masquer des mots-clés malveillants. La technique a été brièvement mentionnée par Microsoft Threat Intelligence en 2021, mais son application généralisée aux objets de courriel semble moins répandue.

Outre la ligne d'objet, le trait d'union conditionnel a également été largement utilisé dans le corps du message pour diviser les mots. Le lien contenu dans ce courriel menait à une page de connexion de messagerie web factice conçue pour voler les identifiants des utilisateurs.

**Points clés :**

*   Utilisation de caractères invisibles (trait d'union conditionnel U+00AD) dans la ligne d'objet des courriels d'hameçonnage.
*   Application de la technique pour contourner les filtres de sécurité analysant les lignes d'objet.
*   Objet encodé via MIME "encoded-word" (UTF-8, Base64) pour masquer les caractères.
*   Le trait d'union conditionnel est également présent dans le corps du message.
*   Le lien du courriel mène à une page de vol d'identifiants.

**Vulnérabilités :**

*   Aucune vulnérabilité spécifique avec un numéro CVE n'est mentionnée dans l'article pour cette technique. La méthode repose sur l'exploitation du comportement des clients de messagerie et des systèmes de filtrage face à des caractères non standards ou découpés.

**Recommandations :**

*   Les solutions de sécurité devraient être mises à jour pour mieux détecter l'utilisation de caractères "invisibles" ou non rendus dans les lignes d'objet.
*   Les utilisateurs doivent rester vigilants face aux courriels, même si la ligne d'objet semble normale, et vérifier attentivement les expéditeurs et les liens.
*   L'implémentation de contrôles de sécurité plus robustes pour l'analyse du contenu des courriels, y compris la détection de caractères encodés de manière inhabituelle, est recommandée.

---
[Source](https://isc.sans.edu/diary/rss/32428){:target="_blank"}
