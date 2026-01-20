---
title: 'Add Punycode to your Threat Hunting Routine, (Tue, Jan 20th)'
date: 2026-01-20
permalink: /posts/2026/01/20/add-punycode-to-your-threat-hunting-routine-tue-jan-20th/
tags:
- veille-cyber
- sans-isc
---
## Utilisation de Punycode dans la Chasse aux Menaces

Les noms de domaine internationalisés (IDN) permettent d'utiliser des caractères non-ASCII dans les adresses web. Bien qu'utiles pour la localisation, ils peuvent être exploités par des attaquants pour créer des URL trompeuses, en substituant des caractères similaires pour induire en erreur les utilisateurs. Par exemple, un "o" grec peut remplacer un "o" latin.

Pour gérer ces caractères spéciaux, les IDN sont encodés en Punycode, un format basé sur des caractères ASCII classiques. Ce format se caractérise par le préfixe "xn--". Par exemple, un domaine utilisant un caractère spécial pourrait être représenté comme `xn--yutube-wqf.com`. Le "xn--" indique qu'il s'agit d'une version encodée, suivi du nom de domaine ASCII classique, puis d'une partie encodée pour les caractères spécifiques.

Il est possible de décoder ces adresses Punycode en utilisant des outils en ligne ou des scripts, comme le montre un exemple en Python. L'analyse de la sortie décodée peut révéler des caractères non standards, indiquant l'utilisation potentielle de caractères non-ASCII.

Bien que tous les IDN ne soient pas malveillants, leur présence inhabituelle dans les journaux de résolution DNS mérite une investigation. La détection de domaines commençant par "xn--" dans les logs DNS constitue une piste précieuse pour la chasse aux menaces, permettant de repérer des activités potentiellement suspectes.

### Points Clés

*   Les IDN peuvent être utilisés dans des attaques par hameçonnage ou tromperie en substituant des caractères visuellement similaires.
*   Le format Punycode est utilisé pour représenter les IDN en utilisant des caractères ASCII, avec un préfixe "xn--".
*   Les adresses Punycode peuvent être décodées pour révéler les caractères originaux, potentiellement non-ASCII.
*   L'analyse des journaux de résolution DNS pour détecter les occurrences de "xn--" est une méthode efficace pour la chasse aux menaces.

### Vulnérabilités

Aucune vulnérabilité spécifique (CVE) n'est directement mentionnée dans cet article, mais la **technique d'usurpation de domaine via des caractères similaires (homoglyphes)** est exploitée.

### Recommandations

*   **Inclure la recherche de noms de domaine encodés en Punycode (préfixe "xn--") dans les routines de chasse aux menaces.**
*   **Surveiller et analyser les journaux de résolution DNS** pour identifier les requêtes suspectes.
*   Utiliser des outils de décodage Punycode pour examiner les domaines potentiellement malveillants.
*   Sensibiliser les utilisateurs aux risques liés aux URL qui semblent inhabituelles ou utilisent des caractères non standards.

---
[Source](https://isc.sans.edu/diary/rss/32640){:target="_blank"}
