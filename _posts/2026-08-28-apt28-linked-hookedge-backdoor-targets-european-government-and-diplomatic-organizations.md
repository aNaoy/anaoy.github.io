---
title: 'APT28-Linked HOOKEDGE Backdoor Targets European Government and Diplomatic Organizations'
date: 2026-08-28
permalink: /posts/2026/08/28/apt28-linked-hookedge-backdoor-targets-european-government-and-diplomatic-organizations/
tags:
- veille-cyber
- hackernews
---
### Menace APT28 : Analyse de la porte dérobée HOOKEDGE

Le groupe APT28 (alias BlueDelta) déploie activement **HOOKEDGE**, une nouvelle porte dérobée légère sous forme de script batch Windows, visant des organisations gouvernementales et diplomatiques en Roumanie, en Espagne et en Turquie. Ce malware succède au programme HEADLACE et se distingue par son utilisation détournée de services légitimes pour ses communications.

**Points clés :**
*   **Vecteur d'attaque :** Documents Microsoft Word piégés avec des macros malveillantes (thématiques diplomatiques).
*   **Infrastructure C2 :** Utilisation abusive du service *webhook.site* pour le pilotage, l'exfiltration de données et le déploiement de charges utiles. Cela permet de masquer l'activité malveillante dans le trafic réseau légitime.
*   **Stratégie :** Mise en place d'une architecture à deux étages pour contourner les limites des quotas du service webhook et maintenir un accès persistant sur les cibles à haute valeur ajoutée.
*   **Opération :** Le malware crée des tâches planifiées, s'exécute via des instances invisibles de Microsoft Edge, puis supprime ses propres traces pour compliquer l'investigation numérique.

**Vulnérabilités :**
*   Aucune CVE spécifique n'est mentionnée, car l'attaque repose sur l'abus de fonctionnalités légitimes (**Macro Microsoft Office**, **Tâches planifiées Windows**) et le détournement de services cloud tiers (*webhook.site*).

**Recommandations :**
*   **Blocage des macros :** Désactiver systématiquement l'exécution des macros pour les documents provenant d'Internet via les stratégies de groupe (GPO).
*   **Surveillance des comportements :** Mettre en place des alertes pour la création suspecte de tâches planifiées et l'exécution de processus Microsoft Edge en mode "headless" (sans interface utilisateur).
*   **Filtrage réseau :** Restreindre ou surveiller les connexions sortantes vers des services de type *webhook.site* ou des domaines de staging non autorisés.
*   **Hygiène de sécurité :** Sensibiliser les utilisateurs aux risques liés aux pièces jointes non sollicitées, particulièrement celles exigeant l'activation du contenu.

---
[Source](https://thehackernews.com/2026/08/apt28-linked-hookedge-backdoor-targets.html){:target="_blank"}
