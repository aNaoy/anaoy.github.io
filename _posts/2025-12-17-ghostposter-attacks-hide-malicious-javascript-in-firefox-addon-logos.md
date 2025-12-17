---
title: 'GhostPoster attacks hide malicious JavaScript in Firefox addon logos'
date: 2025-12-17
permalink: /posts/2025/12/17/ghostposter-attacks-hide-malicious-javascript-in-firefox-addon-logos/
tags:
- veille-cyber
- bleepingcomp
---
## Attaques GhostPoster : Des logos d'extensions Firefox compromis

Une campagne de logiciels malveillants, nommée "GhostPoster", cible les utilisateurs de Firefox en dissimulant du code JavaScript malveillant dans les images de logos d'extensions. Ces extensions, qui ont collectivement plus de 50 000 téléchargements, ont été identifiées comme étant utilisées pour espionner l'activité du navigateur et installer une porte dérobée. Le code caché agit comme un chargeur, récupérant la charge utile principale depuis un serveur distant. Pour échapper à la détection, ce chargement n'intervient que lors d'une tentative sur dix.

Les chercheurs ont découvert 17 extensions compromises dans des catégories populaires telles que les VPN gratuits, les outils de capture d'écran, les prévisions météorologiques et les traducteurs. Bien que les chaînes de chargement des malwares varient, toutes communiquent avec la même infrastructure.

### Points Clés

*   **Méthode d'infection :** Le code malveillant est dissimulé dans le fichier image du logo de l'extension, utilisant des techniques de stéganographie.
*   **Charge utile :** Le code récupéré permet de détourner des liens affiliés, d'injecter du code de suivi, et de commettre des fraudes publicitaires et au clic.
*   **Évasion :** Le chargeur est conçu pour être inactif la plupart du temps, ne récupérant la charge utile que dans 10% des cas pour éviter la surveillance du trafic.
*   **Persistance :** Les opérateurs obtiennent un accès privilégié et persistant au navigateur.
*   **Impact :** L'extension menace la vie privée des utilisateurs et pourrait évoluer vers des menaces plus graves.

### Vulnérabilités

Aucune vulnérabilité spécifique avec un identifiant CVE n'est mentionnée pour l'extension elle-même dans l'article. La vulnérabilité réside dans la manière dont le code malveillant est intégré et exécuté via des extensions approuvées.

### Recommandations

*   **Désinstaller les extensions compromises :** Les utilisateurs des extensions identifiées doivent les supprimer immédiatement de leur navigateur Firefox.
*   **Réinitialiser les mots de passe :** Il est conseillé de réinitialiser les mots de passe des comptes importants par mesure de sécurité.
*   **Vigilance accrue :** Les utilisateurs doivent rester attentifs aux nouvelles menaces et vérifier la réputation des extensions avant de les installer.
*   **Action de Mozilla :** Mozilla a été informé et a agi pour supprimer les extensions malveillantes de sa plateforme. Ils ont également renforcé leurs systèmes automatisés pour détecter et bloquer des attaques similaires à l'avenir.

---
[Source](https://www.bleepingcomputer.com/news/security/ghostposter-attacks-hide-malicious-javascript-in-firefox-addon-logos/){:target="_blank"}
