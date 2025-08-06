---
title: 'WWBN, MedDream, Eclipse vulnerabilities'
date: 2025-08-06
permalink: /posts/2025/08/06/wwbn-meddream-eclipse-vulnerabilities/
tags:
- veille-cyber
- zerodaysfans
---
**Vulnérabilités critiques découvertes dans des plateformes logicielles**

Des chercheurs en cybersécurité ont identifié plusieurs failles de sécurité dans les logiciels WWBN AVideo, MedDream PACS Premium et un module Eclipse ThreadX. Ces vulnérabilités, désormais corrigées par les éditeurs respectifs, auraient pu permettre l'exécution de code arbitraire, l'escalade de privilèges, le vol d'informations sensibles ou des attaques par déni de service.

**Points Clés :**

*   **WWBN AVideo (plateforme de streaming vidéo) :** Cinq vulnérabilités de type Cross-Site Scripting (XSS) permettant l'exécution de JavaScript arbitraire. Deux autres failles, exploitables conjointement, ouvrent la voie à l'exécution de code arbitraire via une condition de concurrence dans la fonction de décompression et une liste noire incomplète pour l'interprétation de fichiers `.phar`.
*   **MedDream PACS Premium (système d'imagerie médicale) :** Une vulnérabilité liée à des permissions par défaut incorrectes permet le déchiffrement d'identifiants stockés dans le registre. Une autre faille dans la fonction de connexion autorise l'escalade de privilèges via l'upload d'un fichier `.php` malveillant. Une vulnérabilité XSS réflectée sur la page `radiationDoseReport.php` permet l'exécution de JavaScript arbitraire via une URL manipulée. Enfin, une faille de Server-Side Request Forgery (SSRF) sur la fonction `cecho.php` peut être déclenchée par une simple requête HTTP non authentifiée.
*   **Eclipse ThreadX FileX (système d'exploitation temps réel embarqué) :** Une vulnérabilité de dépassement de tampon de type "integer underflow" dans le pilote de disque RAM de FileX peut conduire à l'exécution de code via l'envoi de paquets réseau spécifiquement conçus.

**Vulnérabilités Identifiées (avec CVE) :**

*   **WWBN AVideo :**
    *   CVE-2025-46410 (TALOS-2025-2205)
    *   CVE-2025-53084 (TALOS-2025-2206)
    *   CVE-2025-50128 (TALOS-2025-2207)
    *   CVE-2025-36548 (TALOS-2025-2208)
    *   CVE-2025-41420 (TALOS-2025-2209)
    *   CVE-2025-25214 (TALOS-2025-2212) - Condition de concurrence
    *   CVE-2025-48732 (TALOS-2025-2213) - Liste noire incomplète
*   **MedDream PACS Premium :**
    *   CVE-2025-26469 (TALOS-2025-2154) - Permissions par défaut incorrectes
    *   CVE-2025-27724 (TALOS-2025-2156) - Escalade de privilèges
    *   CVE-2025-32731 (TALOS-2025-2176) - XSS réflectée
    *   CVE-2025-24485 (TALOS-2025-2177) - SSRF
*   **Eclipse ThreadX FileX :**
    *   TALOS-2024-2088 - Dépassement de tampon (integer underflow)

**Recommandations :**

Les éditeurs ont publié des mises à jour pour corriger ces failles. Il est fortement recommandé de mettre à jour les logiciels concernés vers les versions patchées afin de se prémunir contre toute exploitation. L'utilisation de règles de détection Snort spécifiques peut aider à identifier les tentatives d'exploitation.

---
[Source](https://blog.talosintelligence.com/wwbn-meddream-eclipse-vulnerabilities/){:target="_blank"}
