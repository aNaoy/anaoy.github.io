---
title: 'North Korean PurpleBravo Campaign Targeted 3,136 IP Addresses via Fake Job Interviews'
date: 2026-01-21
permalink: /posts/2026/01/21/north-korean-purplebravo-campaign-targeted-3136-ip-addresses-via-fake-job-interviews/
tags:
- veille-cyber
- hackernews
---
### Campagne Nord-Coréenne : Exploitation d'Offres d'Emploi pour l'Espionnage

Une campagne d'activités malveillantes attribuée à un groupe nord-coréen, connu sous le nom de PurpleBravo, a ciblé 3 136 adresses IP à travers le monde. Cette opération a mis en évidence l'exploitation de fausses offres d'emploi pour infiltrer des organisations dans divers secteurs, notamment l'intelligence artificielle, la cryptomonnaie, les services financiers, l'informatique, le marketing et le développement logiciel. Les victimes potentielles se situent en Europe, en Asie du Sud, au Moyen-Orient et en Amérique Centrale.

La campagne, également connue sous d'autres noms tels que Contagious Interview, exploite des candidats à la recherche d'emploi en leur proposant de réaliser des tests techniques sur leurs appareils professionnels. Cela crée une exposition de l'entreprise au-delà de l'employé visé, compromettant potentiellement la chaîne d'approvisionnement logicielle.

Des personas LinkedIn falsifiés, se faisant passer pour des recruteurs ou des développeurs, ainsi que des dépôts GitHub malveillants, ont été utilisés pour distribuer des logiciels malveillants, notamment le voleur d'informations et chargeur JavaScript BeaverTail et la porte dérobée basée en Go nommée GolangGhost. Ces activités sont gérées via des serveurs de commande et de contrôle (C2) administrés par le biais du VPN Astrill, une technique fréquemment observée chez les acteurs de menaces nord-coréens.

Cette campagne est distincte mais présente des recoupements tactiques et infrastructurels avec une autre opération nord-coréenne, Wagemole (ou PurpleDelta), qui vise à obtenir des emplois frauduleusement pour des activités d'espionnage et de gain financier. L'infiltration de la chaîne d'approvisionnement logicielle par le biais de ces candidats malveillants représente un risque significatif, en particulier pour les entreprises qui externalisent des services dans les régions touchées.

**Points Clés :**

*   **Cible Principale :** 3 136 adresses IP, visant 20 organisations dans des secteurs sensibles.
*   **Méthode d'Attaque :** Exploitation de fausses offres d'emploi et tests de codage sur des appareils professionnels.
*   **Acteurs Malveillants :** Groupe nord-coréen PurpleBravo.
*   **Période d'Activité :** Principalement d'août 2024 à septembre 2025.
*   **Outils Utilisés :** Personas LinkedIn falsifiés, dépôts GitHub malveillants, BeaverTail (infostealer), GolangGhost (backdoor).
*   **Infrastructure C2 :** Gérée via Astrill VPN et des adresses IP en Chine.
*   **Risque Élargi :** Compromission de la chaîne d'approvisionnement logicielle et fuite potentielle de données sensibles.

**Vulnérabilités :**

*   Aucune vulnérabilité spécifique avec un identifiant CVE n'est mentionnée dans le texte fourni. L'exploitation repose sur l'ingénierie sociale et l'exécution de code par les candidats.

**Recommandations :**

*   Les organisations doivent être vigilantes face aux offres d'emploi suspectes et aux demandes de tests techniques sur des appareils professionnels.
*   Renforcer la sécurité de la chaîne d'approvisionnement logicielle et la surveillance des vulnérabilités potentielles introduites par des tiers.
*   Sensibiliser les employés aux risques d'ingénierie sociale et aux tactiques d'hameçonnage.
*   Mettre en place des processus de vérification robustes pour les nouvelles recrues et les fournisseurs externes.

---
[Source](https://thehackernews.com/2026/01/north-korean-purplebravo-campaign.html){:target="_blank"}
