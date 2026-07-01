---
title: 'The SOC Files: ScreenConnect masked as freeware. An inside look at a large-scale campaign'
date: 2026-07-01
permalink: /posts/2026/07/01/the-soc-files-screenconnect-masked-as-freeware-an-inside-look-at-a-large-scale-campaign/
tags:
- veille-cyber
- securelist
---
### Campagne de malwares massive via détournement d'outils d'administration légitimes

Une campagne cybercriminelle à grande échelle a été identifiée, utilisant des sites web frauduleux imitant des logiciels populaires (OBS Studio, DS4Windows, DNS Jumper, etc.) pour distribuer des archives malveillantes. Ces archives déploient silencieusement l'outil d'accès distant légitime **ScreenConnect** afin de prendre le contrôle des systèmes, d'exfiltrer des données et de déployer le cheval de Troie d'accès distant (RAT) **AsyncRAT**.

**Points clés :**
*   **Tactique SEO :** Les attaquants utilisent le référencement naturel pour placer leurs sites frauduleux en tête des résultats de recherche.
*   **Déguisement :** Les archives contiennent un binaire Microsoft légitime (`install.exe`) détourné par une DLL malveillante (`install.res.1033.dll`) via une technique de *DLL Sideloading*.
*   **Persistance :** L'infection utilise des tâches planifiées et des injections de code dans des processus système (`RegAsm.exe`) pour maintenir une persistance discrète.
*   **Infrastructure :** Le réseau repose sur plus de 90 domaines localisés en plusieurs langues, orchestrés via une infrastructure C2 complexe.
*   **Objectif :** Vol de données d'identification et accès aux systèmes pour une revente sur le dark web.

**Vulnérabilités exploitées :**
*   **T1055.012 (Process Hollowing) :** Injection de code malveillant dans `RegAsm.exe`.
*   **DLL Sideloading :** Utilisation d'une bibliothèque malveillante chargée par un binaire légitime signé par Microsoft.
*   **Absence de contrôle sur le téléchargement :** Exploitation de la confiance des utilisateurs envers les portails de téléchargement et les outils d'administration (ScreenConnect).
*   *(Note : Aucune CVE spécifique n'est mentionnée, l'attaque repose sur l'abus de fonctionnalités légitimes et de mauvaises configurations.)*

**Recommandations :**
*   **Gestion des privilèges et accès :** Mettre en œuvre une liste d'autorisation (allowlisting) stricte pour les applications et bloquer l'exécution de paquets MSI provenant de sources non fiables.
*   **Surveillance proactive :** Surveiller étroitement la création de nouvelles tâches planifiées, l'exécution de scripts PowerShell suspects et l'installation d'outils d'administration à distance non autorisés.
*   **Filtrage réseau :** Bloquer ou filtrer le trafic sortant vers des domaines inconnus ou suspects.
*   **Sensibilisation :** Former les utilisateurs aux risques liés aux téléchargements de logiciels sur des sites tiers et vérifier systématiquement l'authenticité des sources officielles.
*   **Hygiène de sécurité :** Effectuer régulièrement des audits de configuration sur les endpoints pour identifier les exclusions inappropriées dans les solutions antivirus.

---
[Source](https://securelist.com/tr/the-soc-files-screenconnect-campaign-with-asyncrat/120472/){:target="_blank"}
