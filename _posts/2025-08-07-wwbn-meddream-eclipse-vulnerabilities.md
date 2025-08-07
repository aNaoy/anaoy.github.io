---
title: 'WWBN, MedDream, Eclipse vulnerabilities'
date: 2025-08-07
permalink: /posts/2025/08/07/wwbn-meddream-eclipse-vulnerabilities/
tags:
- veille-cyber
- zerodaysfans
---
**Failles de sécurité critiques dans des plateformes logicielles courantes**

Des chercheurs ont identifié un total de onze vulnérabilités affectant les logiciels WWBN AVideo, MedDream PACS Premium et un module d'Eclipse ThreadX. Ces failles, une fois exploitées, peuvent permettre l'exécution de code arbitraire, l'escalade de privilèges, la falsification de requêtes côté serveur et la divulgation d'informations sensibles. Les éditeurs de ces logiciels ont corrigé ces problèmes conformément aux politiques de divulgation de vulnérabilités.

**Points clés et vulnérabilités découvertes :**

*   **WWBN AVideo (Versions 14.4 et dev master commit 8a8954ff) :**
    *   Cinq vulnérabilités de type Cross-Site Scripting (XSS) permettant l'exécution de JavaScript arbitraire dans le navigateur d'un utilisateur :
        *   CVE-2025-46410
        *   CVE-2025-53084
        *   CVE-2025-50128
        *   CVE-2025-36548
        *   CVE-2025-41420
    *   Une vulnérabilité de condition de concurrence (race condition) dans la fonctionnalité de décompression, pouvant mener à l'exécution de code arbitraire :
        *   CVE-2025-25214
    *   Une vulnérabilité de liste noire incomplète dans le fichier .htaccess, permettant l'exécution de code arbitraire via une requête HTTP spécialement conçue :
        *   CVE-2025-48732

*   **MedDream PACS Premium (Versions 7.3.3.840 et 7.3.5.860) :**
    *   Une vulnérabilité de permissions par défaut incorrectes permettant à une application spécialement conçue de déchiffrer des identifiants stockés dans le registre :
        *   CVE-2025-26469
    *   Une vulnérabilité d'escalade de privilèges dans la fonctionnalité `login.php`, permettant l'élévation des capacités via le téléchargement d'un fichier malveillant :
        *   CVE-2025-27724
    *   Une vulnérabilité XSS réfléchie dans la fonctionnalité `radiationDoseReport.php`, permettant l'exécution de JavaScript arbitraire via une URL malveillante :
        *   CVE-2025-32731
    *   Une vulnérabilité de falsification de requête côté serveur (SSRF) dans la fonctionnalité `cecho.php`, permettant à un attaquant d'effectuer des requêtes HTTP non authentifiées vers des ressources internes :
        *   CVE-2025-24485

*   **Eclipse ThreadX FileX (git commit 1b85eb2) :**
    *   Une vulnérabilité de dépassement de tampon (buffer overflow) dans le pilote de disque RAM de FileX, pouvant mener à l'exécution de code via une série de paquets réseau :
        *   TALOS-2024-2088 (pas de CVE spécifié dans l'article)

**Recommandations :**

Les utilisateurs de ces logiciels sont fortement encouragés à mettre à jour leurs systèmes vers les versions corrigées. Pour la détection des tentatives d'exploitation de ces vulnérabilités, il est recommandé de télécharger les dernières règles de détection disponibles sur Snort.org.

---
[Source](https://blog.talosintelligence.com/wwbn-meddream-eclipse-vulnerabilities/){:target="_blank"}
