---
title: 'Survey: 94% of Incidents Involve Anonymized Infrastructure. Teams Are Still Reactive'
date: 2026-06-16
permalink: /posts/2026/06/16/survey-94-of-incidents-involve-anonymized-infrastructure-teams-are-still-reactive/
tags:
- veille-cyber
- hackernews
---
### L'hégémonie des infrastructures anonymisées : passer de la réaction à la décision

Une étude récente menée auprès de 200 experts en cybersécurité révèle que 94 % des incidents impliquent désormais des infrastructures anonymisées, telles que les VPN ou les réseaux de proxys résidentiels. Cette tendance complique la tâche des équipes de sécurité, pour qui la simple réputation IP ne suffit plus à distinguer une activité légitime d'une attaque.

**Points clés :**
* **Invisibilité des attaquants :** Les proxys résidentiels imitent le comportement des utilisateurs normaux, rendant les listes de blocage statiques obsolètes.
* **Déficit de contexte :** Le manque de visibilité sur l'intention derrière une adresse IP est le principal défi opérationnel.
* **Risque interne négligé :** L'usage personnel de VPN ou de proxys sur les appareils des employés crée des angles morts au sein des architectures réseau.
* **Approche réactive :** La plupart des organisations utilisent l'intelligence IP uniquement pour enquêter après coup, plutôt que pour prévenir les menaces en temps réel.

**Vulnérabilités :**
L'article ne mentionne pas de CVE spécifique, mais souligne des vulnérabilités structurelles :
* **Abus d'identifiants (Credential Abuse) :** facilité par la rotation d'adresses IP résidentielles.
* **Prise de contrôle de compte (ATO) :** facilitée par le masquage de l'origine géographique et technique.
* **Défaut de visibilité "Zero Trust" :** absence de contrôle sur l'usage de proxys par les utilisateurs internes.

**Recommandations :**
* **Enrichir le contexte :** Aller au-delà de la géolocalisation en intégrant l'attribution des infrastructures, les indicateurs comportementaux et les données de session.
* **Automatiser les décisions :** Intégrer l'intelligence IP directement dans les flux de travail d'authentification adaptative, de contrôle d'accès basé sur le risque et de prévention de la fraude.
* **Surveiller l'interne :** Traiter l'utilisation de proxys sur les appareils des employés comme un signal de risque, même au sein de réseaux supposés de confiance.
* **Mesurer l'impact opérationnel :** Passer d'indicateurs quantitatifs (volume de menaces bloquées) à des indicateurs qualitatifs (réduction du temps d'enquête et des faux positifs).

---
[Source](https://thehackernews.com/2026/06/survey-94-of-incidents-involve.html){:target="_blank"}
