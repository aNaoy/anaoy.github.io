---
title: 'APT24 Deploys BADAUDIO in Years-Long Espionage Hitting Taiwan and 1,000+ Domains'
date: 2025-11-21
permalink: /posts/2025/11/21/apt24-deploys-badaudio-in-years-long-espionage-hitting-taiwan-and-1000-domains/
tags:
- veille-cyber
- hackernews
---
## APT24 : Une campagne d'espionnage persistante aux multiples facettes

Un groupe de menace lié à la Chine, identifié sous le nom d'APT24 (également connu sous le nom de Pitty Tiger), mène une campagne d'espionnage de longue durée, particulièrement axée sur Taïwan. Les activités récentes de ce groupe mettent en lumière l'utilisation d'un logiciel malveillant inédit appelé BADAUDIO, ainsi que des tactiques sophistiquées d'accès initial.

**Points clés :**

*   **Durée et portée :** La campagne, active depuis près de trois ans, a exploité plus de 1 000 domaines.
*   **Évolution des tactiques :** Initialement axé sur des compromissions web stratégiques, APT24 a récemment intensifié ses attaques via des compromissions de chaîne d'approvisionnement et des campagnes de phishing ciblées.
*   **Ciblage :** Les secteurs visés incluent le gouvernement, la santé, la construction, l'ingénierie, les mines, les organisations à but non lucratif et les télécommunications, principalement aux États-Unis et à Taïwan.
*   **Association avec d'autres groupes :** APT24 est étroitement lié au groupe APT Earth Aughisky.
*   **Nouvelle campagne :** Parallèlement, une autre campagne, nommée "Autumn Dragon", cible des secteurs gouvernementaux, médiatiques et d'information en Asie du Sud-Est, utilisant une vulnérabilité dans WinRAR.

**Vulnérabilités exploitées (avec CVE) :**

*   **Vulnérabilités Office antérieures :**
    *   CVE-2012-0158
    *   CVE-2014-1761
*   **Vulnérabilité WinRAR :**
    *   CVE-2025-8088 (score CVSS : 8.8)
*   **Techniques d'exécution :**
    *   Détournement d'ordre de recherche de DLL (MITRE ATT&CK T1574.001)
    *   Chargement latéral de DLL

**Malwares associés :**

*   **BADAUDIO :** Un logiciel malveillant obfusqué écrit en C++, utilisant la "réduction de flux de contrôle" pour résister à l'ingénierie inverse. Il agit comme un téléchargeur de premier stade, capable de télécharger, décrypter et exécuter une charge utile chiffrée AES. Il est distribué via des archives chiffrées, des pages web compromises (avec du JavaScript conçu pour tromper les utilisateurs en leur faisant croire à une mise à jour de Google Chrome), et des chaînes d'approvisionnement logicielles.
*   **CT RAT, MM RAT (Goldsun-B), Paladin RAT, Leo RAT, Taidoor (Roudan), Specas :** D'autres familles de malwares associées à APT24.
*   **Implant de troisième étape dans la campagne Autumn Dragon :** Un implant léger capable de communiquer avec un serveur distant et d'exécuter huit commandes différentes (exécution de commandes, chargement de DLL, exécution de shellcode, etc.).

**Recommandations (implicites et explicites) :**

*   **Surveillance des activités de phishing :** Vigilance accrue face aux e-mails et documents suspects, notamment ceux exploitant des vulnérabilités logicielles connues.
*   **Sécurisation des chaînes d'approvisionnement :** Examiner attentivement les bibliothèques JavaScript tierces et les scripts utilisés, et maintenir les logiciels à jour.
*   **Protection contre les malwares :** Utiliser des solutions de sécurité robustes et à jour pour détecter et bloquer les malwares comme BADAUDIO.
*   **Correction des vulnérabilités :** Appliquer les correctifs de sécurité dès leur disponibilité, en particulier pour des logiciels couramment utilisés comme WinRAR.
*   **Analyse du trafic réseau :** Surveiller les communications suspectes vers des serveurs de commande et de contrôle (C2).
*   **Conscience des techniques avancées :** Reconnaître les tactiques telles que le détournement de DLL et le chargement latéral de DLL pour une meilleure détection.
*   **Filtrage du contenu web :** Prudence accrue lors de la navigation sur des sites web, en particulier ceux qui demandent des téléchargements sous des prétextes de mises à jour.

---
[Source](https://thehackernews.com/2025/11/apt24-deploys-badaudio-in-years-long.html){:target="_blank"}
