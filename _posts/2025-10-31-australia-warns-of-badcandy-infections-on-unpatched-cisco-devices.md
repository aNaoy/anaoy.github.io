---
title: 'Australia warns of BadCandy infections on unpatched Cisco devices'
date: 2025-10-31
permalink: /posts/2025/10/31/australia-warns-of-badcandy-infections-on-unpatched-cisco-devices/
tags:
- veille-cyber
- bleepingcomp
---
### Infections par BadCandy sur des appareils Cisco non corrigés

Des attaques informatiques sont toujours en cours contre des appareils Cisco utilisant le système d'exploitation IOS XE non mis à jour en Australie. Ces attaques visent à infecter les routeurs avec le webshell BadCandy.

**Points Clés :**

*   La vulnérabilité exploitée (CVE-2023-20198) permet à des acteurs malveillants non authentifiés de créer un utilisateur administrateur local via l'interface utilisateur web, leur donnant ainsi le contrôle total des appareils.
*   Cisco a corrigé cette faille en octobre 2023, mais un exploit public a rapidement suivi, entraînant une exploitation massive pour installer des portes dérobées sur des appareils exposés à Internet.
*   Le webshell BadCandy, une fois installé, permet l'exécution de commandes avec des privilèges root à distance.
*   Bien que le webshell soit supprimé lors du redémarrage, les attaquants peuvent facilement le réinstaller si les appareils ne sont pas corrigés et que l'interface web reste accessible.
*   Des variants de BadCandy sont toujours utilisés dans des attaques en 2024 et 2025, indiquant que de nombreux appareils Cisco restent vulnérables.
*   Des signes de réexploitation de la faille sur les mêmes appareils ont été observés, même après que les entités compromises aient été informées. Les attaquants peuvent détecter le retrait de l'implant et le réintroduire.
*   La faille a été précédemment utilisée par des acteurs étatiques tels que "Salt Typhoon", soupçonnés d'attaques contre des fournisseurs de services de télécommunication aux États-Unis et au Canada.

**Vulnérabilités :**

*   **CVE-2023-20198** : Un défaut de gravité maximale dans l'interface utilisateur web de Cisco IOS XE permettant la création d'un utilisateur administrateur local sans authentification.

**Recommandations :**

*   Les administrateurs de systèmes Cisco IOS XE doivent impérativement appliquer les correctifs fournis par Cisco.
*   Il est conseillé de suivre les recommandations de sécurisation et de durcissement des appareils Cisco IOS XE publiées par Cisco.
*   Les mesures de réponse aux incidents doivent être menées pour les appareils compromis.

---
[Source](https://www.bleepingcomputer.com/news/security/australia-warns-of-badcandy-infections-on-unpatched-cisco-devices/){:target="_blank"}
