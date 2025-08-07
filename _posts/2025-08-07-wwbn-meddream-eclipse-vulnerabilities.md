---
title: 'WWBN, MedDream, Eclipse vulnerabilities'
date: 2025-08-07
permalink: /posts/2025/08/07/wwbn-meddream-eclipse-vulnerabilities/
tags:
- veille-cyber
- zerodaysfans
---
**Cyberattaques : Vulnérabilités dans WWBN, MedDream et Eclipse ThreadX**

Une analyse récente a révélé un total de douze failles de sécurité critiques affectant trois logiciels distincts : WWBN AVideo, MedDream PACS Premium et un module d'Eclipse ThreadX. Ces vulnérabilités, découvertes par l'équipe de Cisco Talos, ont été corrigées par les éditeurs respectifs.

**Points clés :**

*   **WWBN AVideo :** Cinq vulnérabilités de script inter-sites (XSS) permettent l'exécution de JavaScript arbitraire. De plus, une condition de concurrence et une liste noire incomplète, lorsqu'elles sont combinées, peuvent conduire à l'exécution de code arbitraire.
*   **MedDream PACS Premium :** Quatre vulnérabilités ont été identifiées, incluant une mauvaise gestion des permissions par défaut permettant le déchiffrement d'identifiants, une escalade de privilèges via l'upload de fichiers malveillants, une vulnérabilité XSS dans le rapport de dose de rayonnement, et une faille de falsification de requête côté serveur (SSRF).
*   **Eclipse ThreadX FileX :** Une seule vulnérabilité de dépassement de tampon (buffer overflow) liée à un sous-dépassement d'entier dans le pilote de disque RAM a été découverte.

**Vulnérabilités identifiées :**

*   **WWBN AVideo :**
    *   TALOS-2025-2205 (CVE-2025-46410) : XSS
    *   TALOS-2025-2206 (CVE-2025-53084) : XSS
    *   TALOS-2025-2207 (CVE-2025-50128) : XSS
    *   TALOS-2025-2208 (CVE-2025-36548) : XSS
    *   TALOS-2025-2209 (CVE-2025-41420) : XSS
    *   TALOS-2025-2212 (CVE-2025-25214) : Condition de concurrence menant à l'exécution de code arbitraire
    *   TALOS-2025-2213 (CVE-2025-48732) : Liste noire incomplète menant à l'exécution de code arbitraire
*   **MedDream PACS Premium :**
    *   TALOS-2025-2154 (CVE-2025-26469) : Mauvaise gestion des permissions par défaut
    *   TALOS-2025-2156 (CVE-2025-27724) : Escalade de privilèges
    *   TALOS-2025-2176 (CVE-2025-32731) : XSS réfléchi
    *   TALOS-2025-2177 (CVE-2025-24485) : SSRF
*   **Eclipse ThreadX FileX :**
    *   TALOS-2024-2088 : Dépassement de tampon (sous-dépassement d'entier)

**Recommandations :**

Les utilisateurs sont fortement encouragés à appliquer les correctifs fournis par les éditeurs des logiciels affectés. Des règles Snort sont disponibles pour la détection de l'exploitation de ces vulnérabilités.

---
[Source](https://blog.talosintelligence.com/wwbn-meddream-eclipse-vulnerabilities/){:target="_blank"}
