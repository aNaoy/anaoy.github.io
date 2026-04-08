---
title: '13-year-old bug in ActiveMQ lets hackers remotely execute commands'
date: 2026-04-08
permalink: /posts/2026/04/08/13-year-old-bug-in-activemq-lets-hackers-remotely-execute-commands/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilité critique découverte dans Apache ActiveMQ via l'IA

Une vulnérabilité vieille de 13 ans a été identifiée dans Apache ActiveMQ Classic, permettant à un attaquant d'exécuter des commandes à distance (RCE). Cette faille, découverte à l'aide de l'IA (Claude), démontre comment l'interaction entre des composants isolés et sécurisés peut créer un chemin d'attaque critique.

**Points clés :**
* **Origine :** La vulnérabilité réside dans l'API de gestion Jolokia, qui permet le chargement de configurations externes via la fonction `addNetworkConnector`.
* **Mécanisme :** En envoyant une requête spécifique, un attaquant peut forcer le courtier (broker) à charger un fichier de configuration Spring XML distant, entraînant l'exécution de commandes système arbitraires.
* **Détection par l'IA :** Le chercheur a utilisé Claude pour analyser les interactions entre Jolokia, JMX et les transporteurs réseau, révélant une faille restée indétectable par les méthodes traditionnelles pendant plus d'une décennie.

**Vulnérabilités associées :**
* **CVE-2026-34197 (Score 8.8) :** Affecte ActiveMQ Classic avant la version 5.19.4 et de 6.0.0 à 6.2.3.
* **CVE-2024-32114 :** Bug complémentaire rendant l'API Jolokia accessible sans authentification sur certaines versions (6.0.0 à 6.1.1), augmentant drastiquement le risque.

**Recommandations :**
* **Mise à jour immédiate :** Appliquer les correctifs publiés par Apache dans les versions **5.19.4** et **6.2.3**.
* **Surveillance des logs :** Rechercher des connexions suspectes utilisant le protocole de transport interne `VM` couplées au paramètre `brokerConfig=xbean:http://`.
* **Analyse des signes d'exploitation :** Un message d'avertissement concernant un problème de configuration dans les logs indique que la charge utile a potentiellement déjà été exécutée.

---
[Source](https://www.bleepingcomputer.com/news/security/13-year-old-bug-in-activemq-lets-hackers-remotely-execute-commands/){:target="_blank"}
