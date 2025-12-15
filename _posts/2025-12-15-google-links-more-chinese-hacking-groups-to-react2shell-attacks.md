---
title: 'Google links more Chinese hacking groups to React2Shell attacks'
date: 2025-12-15
permalink: /posts/2025/12/15/google-links-more-chinese-hacking-groups-to-react2shell-attacks/
tags:
- veille-cyber
- bleepingcomp
---
**Vague menace chinoise sur les applications React**

Plusieurs groupes de pirates informatiques chinois exploitent une vulnérabilité critique nommée "React2Shell" dans les bibliothèques JavaScript React et les frameworks tels que Next.js. Cette faille permet l'exécution de code à distance sans authentification via une simple requête HTTP. Google Threat Intelligence a identifié cinq groupes supplémentaires impliqués dans ces attaques, portant le total à plusieurs entités liées à des activités d'espionnage et de cybercriminalité. Les attaquants ciblent des données sensibles, des identifiants et des fichiers de configuration cloud. D'autres acteurs, y compris des groupes iraniens et des mineurs de cryptomonnaies, profitent également de cette vulnérabilité. Des milliers d'adresses IP sont exposées, principalement aux États-Unis. Un incident majeur a causé une interruption mondiale des services pour Cloudflare suite à des mesures d'urgence contre cette menace.

**Points Clés :**

*   **Vulnérabilité :** React2Shell (CVE-2025-55182) affecte les versions 19.0 à 19.2.0 de React et est présente par défaut dans certains modules comme `react-server-dom-parcel`, `react-server-dom-turbopack`, et `react-server-dom-webpack`.
*   **Acteurs :** Au moins cinq groupes de pirates informatiques chinois, dont UNC6600, UNC6586, UNC6588, UNC6603 et UNC6595, sont impliqués, en plus des groupes déjà identifiés comme Earth Lamia et Jackpot Panda. Des acteurs iraniens et des groupes motivés par des gains financiers ont également été observés.
*   **Impact :** Permet l'exécution de code à distance sans authentification, le vol d'informations sensibles (fichiers de configuration AWS, identifiants) et le déploiement de logiciels malveillants (logiciels de tunneling, backdoors, RATs, mineurs de cryptomonnaies).
*   **Diffusion :** Des discussions et des outils d'exploitation sont partagés sur des forums clandestins. Plus de 116 000 adresses IP sont considérées comme vulnérables.

**Vulnérabilités :**

*   **CVE-2025-55182 :** React2Shell - Vulnérabilité critique d'exécution de code à distance dans React et Next.js.

**Recommandations :**

*   **Mise à jour :** Appliquer les correctifs de sécurité dès que possible pour les versions vulnérables de React et des frameworks associés.
*   **Surveillance :** Renforcer la surveillance des réseaux pour détecter les activités suspectes liées à l'exploitation de cette faille.
*   **Sécurisation :** Examiner et sécuriser les configurations par défaut des paquets React affectés.

---
[Source](https://www.bleepingcomputer.com/news/security/google-links-more-chinese-hacking-groups-to-react2shell-attacks/){:target="_blank"}
