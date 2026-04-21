---
title: 'KelpDAO suffers $290 million heist tied to Lazarus hackers'
date: 2026-04-21
permalink: /posts/2026/04/21/kelpdao-suffers-290-million-heist-tied-to-lazarus-hackers/
tags:
- veille-cyber
- bleepingcomp
---
### Piratage massif de KelpDAO : 290 millions de dollars dérobés par Lazarus

Le protocole DeFi KelpDAO a subi un vol de 290 millions de dollars en jetons rsETH, entraînant des répercussions sur les plateformes Compound, Euler et Aave. L'attaque est attribuée au groupe Lazarus (Corée du Nord), spécialisé dans les opérations sophistiquées ciblant les infrastructures de cryptomonnaies.

**Points clés** :
*   **Mode opératoire** : Les attaquants ont ciblé la couche de vérification (DVN) du protocole inter-chaînes LayerZero.
*   **Technique d'injection** : Les pirates ont compromis des nœuds RPC pour injecter de fausses données de blockchain tout en menant simultanément une attaque par déni de service (DDoS) sur les nœuds sains. Cela a forcé le système à valider des messages frauduleux permettant le transfert non autorisé de jetons rsETH.
*   **Blanchiment** : Les fonds dérobés (environ 116 500 rsETH) ont été transférés via le service Tornado Cash pour masquer leur origine.
*   **Impact** : Bien que majeur, l'incident a été isolé au jeton rsETH, sans propagation systémique aux autres actifs.

**Vulnérabilités** :
*   **Exploitation de la confiance RPC** : Dépendance critique envers des nœuds RPC externes pouvant être manipulés.
*   **Faiblesse de la couche de validation (DVN)** : Absence de résilience contre l'alimentation en données corrompues lorsque les nœuds légitimes sont inaccessibles par DDoS.
*   *Note : Aucune CVE spécifique n'est associée à cet incident, l'attaque exploitant la logique métier et l'infrastructure réseau du protocole plutôt qu'une faille logicielle répertoriée.*

**Recommandations** :
*   **Diversification des nœuds RPC** : Ne pas dépendre d'un nombre restreint de nœuds et mettre en place des mécanismes de consensus pour valider les données provenant de multiples sources indépendantes.
*   **Renforcement de la résilience réseau** : Implémenter des protections robustes contre les attaques DDoS sur les composants critiques de l'infrastructure d'interopérabilité.
*   **Surveillance proactive** : Renforcer la détection des anomalies sur les messages inter-chaînes pour identifier et bloquer instantanément les transactions suspectes avant leur finalisation.
*   **Audit des couches de validation** : Revoir les protocoles de vérification décentralisés pour s'assurer qu'ils ne puissent pas être détournés par la saturation forcée de leurs sources de données.

---
[Source](https://www.bleepingcomputer.com/news/security/kelpdao-suffers-290-million-heist-tied-to-lazarus-hackers/){:target="_blank"}
