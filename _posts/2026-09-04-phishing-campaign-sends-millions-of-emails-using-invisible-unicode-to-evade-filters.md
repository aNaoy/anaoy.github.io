---
title: 'Phishing Campaign Sends Millions of Emails Using Invisible Unicode to Evade Filters'
date: 2026-09-04
permalink: /posts/2026/09/04/phishing-campaign-sends-millions-of-emails-using-invisible-unicode-to-evade-filters/
tags:
- veille-cyber
- hackernews
---
### Évasion de filtres e-mail : la menace du "Smuggling ASCII"

Une campagne de phishing massive utilise des caractères Unicode invisibles pour contourner les filtres de sécurité des messageries. Cette technique, baptisée « ASCII Smuggling », consiste à insérer des caractères de la plage Unicode « Tags » (U+E0000 à U+E007F) au sein de mots-clés financiers (ex: « funding » devient « fun[caractère invisible]ding »). Si le texte reste parfaitement lisible pour l'utilisateur humain, il brise les signatures détectées par les systèmes de filtrage automatisés.

**Points clés :**
*   **Volume massif :** La campagne a généré jusqu'à 2,37 millions d'e-mails par jour, avec une activité concentrée sur les jours ouvrés.
*   **Détournement d'outils légitimes :** Les attaquants exploitent la plateforme d'automatisation marketing *ActiveCampaign* pour envoyer des e-mails via des domaines réputés, rendant la détection par réputation d'IP plus difficile.
*   **Objectifs :** Vol d'informations financières et professionnelles, souvent via des leurres liés aux prêts aux petites entreprises (SBA).
*   **Évolution des menaces :** Cette technique illustre l'adaptation des méthodes d'injection de prompts utilisées en IA vers le phishing traditionnel.

**Vulnérabilités :**
*   **Absence de normalisation Unicode :** Les filtres de sécurité ne traitent pas systématiquement la suppression ou la normalisation des caractères invisibles (Unicode Tags) avant l'analyse des chaînes de caractères.
*   **Gestion des boundaries LLM :** Les modèles de langage peinent à distinguer les instructions malveillantes dissimulées dans des données apparemment bénignes.
*   *Note : Aucune CVE spécifique n'est associée à cette technique d'évasion, car il s'agit d'un détournement de fonctionnalités standards des jeux de caractères.*

**Recommandations :**
*   **Normalisation des contenus :** Mettre à jour les passerelles de messagerie pour normaliser systématiquement les e-mails entrants en supprimant les caractères Unicode non imprimables ou suspects avant l'analyse par les moteurs de détection.
*   **Analyse comportementale :** Renforcer les systèmes de détection pour traiter l'utilisation massive de caractères de contrôle (Unicode Tags) comme un signal de haute suspicion, indépendamment du contenu textuel.
*   **Filtrage par réputation :** Ne pas se fier uniquement à la réputation des domaines d'envoi (comme ceux d'ActiveCampaign), mais croiser ces données avec des analyses structurelles du corps du message.

---
[Source](https://thehackernews.com/2026/09/phishing-campaign-sends-millions-of.html){:target="_blank"}
