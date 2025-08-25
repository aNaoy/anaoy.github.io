---
title: 'How Deep Research Agents Can Leak Your Data'
date: 2025-08-25
permalink: /posts/2025/08/25/how-deep-research-agents-can-leak-your-data/
tags:
- veille-cyber
- zerodaysfans
---
**Fuite de Données via les Agents de Recherche Autonomes : Risques et Prévention**

Les agents d'IA dotés de capacités de recherche approfondie, comme ChatGPT avec ses connecteurs, peuvent involontairement exposer des données sensibles en les partageant entre différents outils intégrés. Cette recherche met en lumière que tous les outils connectés opèrent dans une limite de confiance partagée, permettant à l'IA de transférer des informations d'une source à une autre lors de ses recherches autonomes, qui peuvent durer plusieurs minutes sans supervision humaine.

**Points Clés :**

*   **Frontière de Confiance Partagée :** Les données accessibles à un agent depuis une source peuvent être divulguées à d'autres sources lorsque l'agent effectue des requêtes de recherche approfondie.
*   **Vulnérabilité à l'Injection de Prompts :** Un attaquant peut exploiter cette caractéristique via des injections de prompts pour forcer les fuites de données ou manipuler le comportement de l'agent.
*   **Combinaison d'Informations :** L'agent peut agréger des informations provenant de diverses sources, y compris des détails sensibles comme des identifiants ou des informations de production, pour les transmettre à d'autres outils.
*   **Impact des Prompts Injection Antérieurs :** Des instructions malveillantes présentes dans des tickets ou des descriptions d'outils peuvent influencer le processus de recherche de l'IA, entraînant des actions inattendues.

**Scénarios de Fuite Démontrés :**

*   Un ticket avec des instructions spécifiques, incorporé dans le processus de recherche, peut amener l'IA à interagir avec des outils de manière non désirée, transférant des données sensibles (par exemple, d'un outil de gestion de tickets à un serveur MCP personnalisé).
*   Une description d'outil malveillante, incluant des éléments d'injection de prompt, a permis à l'IA de communiquer dans un style spécifique tout en transférant des informations sensibles issues d'autres sources.
*   Des "souvenirs" ou historiques de conversation peuvent également être envoyés à d'autres outils intégrés.

**Recommandations :**

*   **Prudence dans la Configuration des Intégrations :** N'activez que les outils et les sources de données que vous approuvez et dont vous êtes sûr qu'elles ne présenteront pas de risques. Évitez de connecter simultanément des sources de données sensibles avec des sources de données de faible intégrité.
*   **Analyse du Risque :** Avant d'activer des fonctionnalités comme la recherche sur le web (qui peut utiliser Bing et Shopify), évaluez votre tolérance au risque concernant le partage d'informations.
*   **Vérification des Politiques de Confidentialité :** Assurez-vous d'être à l'aise avec les politiques de confidentialité et de protection des données de tous les outils que vous ajoutez, car ils peuvent recevoir des données provenant d'autres invocations d'outils.
*   **Méfiance envers les Connecteurs Tiers :** Soyez particulièrement prudent avec les connecteurs tiers, qui peuvent avoir des effets secondaires supplémentaires et être la cible d'injections de prompts pour détourner l'IA.
*   **Surveillance de l'Activité :** Utilisez le volet récapitulatif dans ChatGPT pour observer quels outils sont invoqués et quelles données leur sont envoyées, afin d'avoir une idée de ce que fait l'agent.

---
[Source](https://embracethered.com/blog/posts/2025/chatgpt-deep-research-connectors-data-spill-and-leaks/){:target="_blank"}
