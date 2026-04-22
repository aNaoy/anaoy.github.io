---
title: 'Harvester Deploys Linux GoGra Backdoor in South Asia Using Microsoft Graph API'
date: 2026-04-22
permalink: /posts/2026/04/22/harvester-deploys-linux-gogra-backdoor-in-south-asia-using-microsoft-graph-api/
tags:
- veille-cyber
- hackernews
---
### Expansion du groupe Harvester : Une nouvelle backdoor Linux exploitant l'API Microsoft Graph

Le groupe de cyberespionnage **Harvester**, actif depuis 2021 et spécialisé dans les secteurs technologiques et gouvernementaux en Asie du Sud, a étendu ses capacités en développant une variante Linux de sa backdoor **GoGra**. 

**Points clés :**
* **Technique de C2 furtive :** Le malware utilise l'API Microsoft Graph et des boîtes mail Outlook légitimes pour communiquer, contournant ainsi les défenses périmétriques traditionnelles.
* **Mode opératoire :** Les attaquants utilisent l'ingénierie sociale pour inciter les victimes à exécuter des binaires ELF déguisés en documents PDF.
* **Mécanisme d'action :** La backdoor interroge un dossier Outlook spécifique ("Zomato Pizza") toutes les deux secondes. Elle exécute des commandes reçues par email (objet commençant par "Input"), renvoie le résultat via un mail intitulé "Output", puis supprime les traces.
* **Attribution :** La persistance d'erreurs orthographiques identiques entre les versions Windows et Linux confirme que le développement est orchestré par les mêmes acteurs.

**Vulnérabilités :**
Aucune CVE spécifique n'est associée, car cette menace repose sur l'abus de fonctionnalités légitimes de l'API Microsoft Graph plutôt que sur l'exploitation d'une faille logicielle.

**Recommandations :**
* **Sensibilisation :** Former les utilisateurs à la méfiance vis-à-vis des documents suspects, particulièrement les fichiers présentés comme des PDF mais possédant une structure d'exécutable (binaires ELF sous Linux).
* **Surveillance réseau :** Surveiller les flux inhabituels vers les APIs Microsoft Cloud, notamment les requêtes OData répétitives provenant d'hôtes qui n'ont pas de raison légitime de communiquer avec ces services.
* **Sécurité des endpoints :** Utiliser des solutions EDR capables de détecter l'exécution de processus suspects et l'utilisation détournée de services cloud pour le contrôle et commande (C2).
* **Filtrage des emails :** Mettre en place des règles de détection sur les boîtes mail professionnelles pour repérer les messages contenant des commandes shell encodées en Base64 ou des échanges suspects de type "Input/Output".

---
[Source](https://thehackernews.com/2026/04/harvester-deploys-linux-gogra-backdoor.html){:target="_blank"}
