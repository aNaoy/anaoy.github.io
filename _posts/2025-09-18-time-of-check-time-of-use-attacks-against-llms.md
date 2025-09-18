---
title: 'Time-of-Check Time-of-Use Attacks Against LLMs'
date: 2025-09-18
permalink: /posts/2025/09/18/time-of-check-time-of-use-attacks-against-llms/
tags:
- veille-cyber
- schneier
---
**Vulnérabilités TOCTOU dans les Agents Basés sur les LLM**

Une recherche récente explore les failles de sécurité de type "Time-of-Check to Time-of-Use" (TOCTOU) dans les agents alimentés par des grands modèles linguistiques (LLM). Contrairement aux attaques par injection de prompt ou par exfiltration de données, ces vulnérabilités surviennent lorsque l'agent vérifie un état externe (comme un fichier ou une réponse d'API) qui est ensuite modifié avant d'être utilisé. Cela peut mener à des attaques pratiques comme le remplacement de configurations malveillantes ou l'injection de charges utiles.

**Points Clés :**

*   Les agents basés sur les LLM sont de plus en plus utilisés, mais introduisent de nouvelles vulnérabilités.
*   Les attaques TOCTOU, largement inexplorées dans ce contexte, exploitent un décalage temporel entre la vérification et l'utilisation d'un état externe.
*   Une nouvelle base d'évaluation, TOCTOU-Bench, a été créée avec 66 tâches réalistes pour étudier ces vulnérabilités.
*   Des techniques de détection et de mitigation issues de la sécurité système ont été adaptées.

**Vulnérabilités :**

*   Non spécifié dans l'article, mais le concept de TOCTOU implique que des modifications non autorisées d'un état externe entre sa vérification et son utilisation par l'agent peuvent compromettre le système.
*   Aucun CVE spécifique n'est mentionné dans cet extrait.

**Recommandations :**

*   **Réécriture de prompt :** Modifier les requêtes pour renforcer la sécurité.
*   **Surveillance de l'intégrité de l'état :** Vérifier l'état des données tout au long de leur utilisation.
*   **Fusing d'outils :** Combiner des outils de manière sécurisée.

L'étude a montré que ces méthodes peuvent atteindre jusqu'à 25 % de précision dans la détection, réduire de 3 % la génération de plans vulnérables, et diminuer la fenêtre d'attaque de 95 %. En combinant les trois approches, la réduction des vulnérabilités TOCTOU dans une trajectoire exécutée passe de 12 % à 8 %. Ces découvertes ouvrent une nouvelle voie de recherche à l'intersection de la sécurité de l'IA et de la sécurité des systèmes.

---
[Source](https://www.schneier.com/blog/archives/2025/09/time-of-check-time-of-use-attacks-against-llms.html){:target="_blank"}
