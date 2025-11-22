---
title: 'China-Linked APT31 Launches Stealthy Cyberattacks on Russian IT Using Cloud Services'
date: 2025-11-22
permalink: /posts/2025/11/22/china-linked-apt31-launches-stealthy-cyberattacks-on-russian-it-using-cloud-services/
tags:
- veille-cyber
- hackernews
---
## APT31 : L'ombre chinoise plane sur le secteur informatique russe

Entre 2024 et 2025, le groupe de cyberespionnage APT31, lié à la Chine, a mené des attaques sophistiquées et discrètes contre le secteur des technologies de l'information en Russie. Ces actions, visant particulièrement les entreprises sous-traitant pour les agences gouvernementales, se sont déroulées sur de longues périodes sans être détectées.

APT31, également connu sous divers autres noms, est actif depuis au moins 2010 et cible un large éventail de secteurs pour le compte de Pékin et de ses entreprises d'État, dans le but d'obtenir des avantages politiques, économiques et militaires.

Les attaques contre la Russie se caractérisent par l'utilisation de services cloud légitimes, notamment Yandex Cloud, pour le commandement et le contrôle (C2) ainsi que pour l'exfiltration de données, afin de se fondre dans le trafic normal. Les attaquants ont également dissimulé des commandes et des charges utiles chiffrées sur des profils de réseaux sociaux et mené leurs opérations durant les week-ends et jours fériés.

Dans au moins une attaque repérée en décembre 2024, APT31 a utilisé un courriel d'hameçonnage contenant une archive RAR. Celle-ci incluait un raccourci Windows (LNK) déclenchant un chargeur Cobalt Strike nommé CloudyLoader via une technique de "DLL side-loading". D'autres techniques observées impliquent des archives ZIP se faisant passer pour des rapports officiels pour déployer également CloudyLoader.

Le groupe a exploité une large gamme d'outils publics et personnalisés pour maintenir sa présence et sa persistance, notamment via des tâches planifiées mimant des applications légitimes.

### Points Clés

*   **Cible:** Secteur des technologies de l'information en Russie, incluant les sous-traitants des agences gouvernementales.
*   **Acteur:** APT31 (Altair, Bronze Vinewood, etc.), groupe de cyberespionnage lié à la Chine.
*   **Période d'activité observée:** Entre 2024 et 2025 (avec des intrusions remontant à fin 2022).
*   **Méthodologie:** Utilisation de services cloud légitimes (Yandex Cloud, Microsoft OneDrive) pour le C2 et l'exfiltration, dissimulation sur les réseaux sociaux, attaques pendant les périodes de faible activité.
*   **Objectif:** Cyberespionnage et collecte d'informations pour le compte de la Chine.

### Vulnérabilités Exploités

Bien que l'article ne mentionne pas explicitement de CVE spécifiques, les méthodes d'attaques révèlent l'exploitation de plusieurs points faibles :

*   **Hameçonnage (Phishing):** Utilisation d'e-mails malveillants pour initier l'infection.
*   **Téléchargement de malware via archives :** Exploitation de vulnérabilités dans le traitement de formats d'archives (RAR, ZIP) pour dissimuler des charges utiles.
*   **Exécution de code arbitraire :** Le raccourci LNK et la technique de "DLL side-loading" permettent l'exécution de code non autorisé.
*   **Utilisation de services légitimes à des fins malveillantes :** Contournement des défenses en exploitant des plateformes cloud et des services de communication courants.
*   **Manque de surveillance du trafic réseau :** L'utilisation de protocoles et de services standards rend la détection difficile.

### Recommandations

*   **Renforcer la surveillance du trafic réseau :** Mettre en place des outils et des procédures pour détecter les communications sortantes vers des services cloud non autorisés ou suspectés.
*   **Sensibilisation à l'hameçonnage :** Former régulièrement les employés à reconnaître et signaler les tentatives d'hameçonnage, notamment celles utilisant des pièces jointes suspectes.
*   **Gestion des privilèges :** Appliquer le principe du moindre privilège pour limiter l'impact d'une éventuelle compromission.
*   **Sécurisation des points d'accès :** Renforcer la sécurité autour des services accessibles depuis l'extérieur et surveiller les tentatives d'accès inhabituelles.
*   **Analyse des logs :** Mettre en place une journalisation complète et une analyse proactive des journaux d'événements pour identifier les activités suspectes.
*   **Mise à jour des systèmes et applications :** S'assurer que tous les logiciels, y compris les bibliothèques et les utilitaires, sont à jour pour corriger les vulnérabilités connues.
*   **Segmentation du réseau :** Limiter la propagation latérale des menaces en segmentant le réseau.
*   **Utilisation d'outils de détection avancée :** Déployer des solutions de sécurité capables de détecter les comportements anormaux et les techniques d'évasion.

---
[Source](https://thehackernews.com/2025/11/china-linked-apt31-launches-stealthy.html){:target="_blank"}
