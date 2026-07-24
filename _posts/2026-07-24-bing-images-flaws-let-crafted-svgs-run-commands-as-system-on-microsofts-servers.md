---
title: 'Bing Images Flaws Let Crafted SVGs Run Commands as SYSTEM on Microsofts Servers'
date: 2026-07-24
permalink: /posts/2026/07/24/bing-images-flaws-let-crafted-svgs-run-commands-as-system-on-microsofts-servers/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans le traitement d'images de Bing

Une faille de sécurité majeure dans le moteur de recherche d'images de Bing a permis à des attaquants d'exécuter des commandes arbitraires avec les privilèges `NT AUTHORITY\SYSTEM` sur les serveurs Windows de Microsoft et `root` sur les serveurs Linux. L'attaque exploitait la manière dont les outils de traitement d'image (compatibles avec ImageMagick) gèrent les fichiers SVG malveillants, en interprétant des références internes comme des commandes système via des "délégués" externes.

**Points clés :**
*   **Vecteurs d'attaque :** La vulnérabilité était exploitable via l'upload direct d'une image SVG ou via l'analyse par le crawler de Bing (`bingbot`) d'une URL contenant un SVG piégé.
*   **Mécanisme :** Le système de traitement d'images, en traitant le SVG, suivait des références externes qui, en raison d'une mauvaise configuration, étaient redirigées vers un shell système au lieu d'être traitées comme de simples fichiers.
*   **Absence d'action utilisateur :** Les correctifs ont été déployés côté serveur par Microsoft dès mars 2024 ; aucune intervention de la part des utilisateurs n'est nécessaire.

**Vulnérabilités identifiées :**
*   **CVE-2026-32194 :** Injection de commandes (CWE-77) via l'upload direct de fichiers SVG.
*   **CVE-2026-32191 :** Injection de commandes système (CWE-78) via le crawler de Bing traitant une URL distante.
*   *Score CVSS : 9.8 (Critique).*

**Recommandations pour sécuriser les services de traitement d'image :**
*   **Désactiver les délégués :** Configurer `policy.xml` d'ImageMagick pour interdire explicitement l'exécution de délégués (`<policy domain="delegate" rights="none" pattern="*" />`).
*   **Restreindre les formats :** Limiter les formats d'image acceptés et bannir les formats complexes (SVG, MVG, EPS) s'ils ne sont pas strictement nécessaires.
*   **Sandboxing :** Exécuter les outils de conversion dans des environnements isolés (sandboxed) avec des privilèges minimaux.
*   **Isolation réseau :** Bloquer les accès sortants (outbound) des serveurs de traitement d'image vers Internet ou vers des réseaux internes sensibles.
*   **Filtrage :** Mettre en place une liste blanche pour les destinations accessibles lors de la récupération d'images par le serveur.

---
[Source](https://thehackernews.com/2026/07/bing-images-flaws-let-crafted-svgs-run.html){:target="_blank"}
