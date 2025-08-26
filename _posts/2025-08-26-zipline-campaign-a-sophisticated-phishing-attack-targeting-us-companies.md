---
title: 'ZipLine Campaign: A Sophisticated Phishing Attack Targeting US Companies'
date: 2025-08-26
permalink: /posts/2025/08/26/zipline-campaign-a-sophisticated-phishing-attack-targeting-us-companies/
tags:
- veille-cyber
- zerodaysfans
---
### Camouflage Numérique : L'Embuscade ZipLine

Une campagne sophistiquée d'ingénierie sociale, baptisée ZipLine, cible des entreprises américaines critiques dans le secteur manufacturier. Elle se distingue par une approche inversée : les attaquants initient le contact via le formulaire "Contactez-nous" du site web de la cible, ce qui amène la victime à initier la correspondance par e-mail, conférant ainsi une fausse légitimité à l'échange. Les discussions durent plusieurs semaines, portant sur des sujets d'affaires légitimes, parfois sur des thèmes comme la "transformation IA".

L'objectif est de livrer une charge utile malveillante sous forme d'archive ZIP. Cette archive contient un script PowerShell injecté dans ses données binaires. Un chargeur PowerShell extrait ensuite ce script pour l'exécuter en mémoire, déployant "MixShell", un implant furtif utilisé pour le contrôle à distance.

**Points Clés :**

*   **Initiation inversée :** Les victimes contactent les attaquants via un formulaire web.
*   **Ingénierie sociale prolongée :** Les conversations durent des semaines pour établir la confiance.
*   **Pretextes variés :** Utilisation de thèmes comme la "transformation IA" ou des propositions de NDA.
*   **Infrastructure déguisée :** Domaines enregistrés correspondant à des LLC américaines, souvent des domaines abandonnés mais légitimes historiquement.
*   **Chargement en mémoire :** L'implant MixShell est exécuté en mémoire pour éviter la détection sur disque.
*   **Communication C2 furtive :** Utilisation du tunneling DNS TXT avec un repli HTTP.

**Vulnérabilités exploitées :**

*   **Ingénierie sociale :** Exploitation de la confiance par des conversations prolongées et des thèmes d'actualité.
*   **Abus de plateformes légitimes :** Hébergement des charges utiles sur des sous-domaines de `herokuapp.com`.
*   **Techniques d'évasion d'antivirus :** Exécution en mémoire, contournement AMSI.
*   **Persistance :** Exploitation de la technique de "TypeLib hijacking" via des clés de registre COM pour garantir une exécution automatique au démarrage.

**Recommandations :**

*   **Prudence accrue avec les communications entrantes :** Ne pas se fier uniquement à la légitimité apparente des canaux de communication entrants, y compris les formulaires web.
*   **Analyse approfondie des communications :** Examiner le contexte et le comportement des échanges par e-mail, même s'ils semblent légitimes.
*   **Solutions de sécurité multicouches :** Utiliser des outils capables d'analyser le contexte des communications, de vérifier les liens et de détecter les comportements suspects dans les pièces jointes.
*   **Vérification de l'infrastructure :** Être vigilant quant à la réputation et à l'historique des domaines et des adresses IP avec lesquels les entreprises interagissent.
*   **Sensibilisation des employés :** Former les équipes à reconnaître les tactiques d'ingénierie sociale, même celles qui sont plus subtiles et prolongées.

---
[Source](https://research.checkpoint.com/2025/zipline-phishing-campaign/){:target="_blank"}
