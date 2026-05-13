---
title: 'Proxying the Unproxyable&#x3f; Sending EXE traffic to a Proxy, (Wed, May 13th)'
date: 2026-05-13
permalink: /posts/2026/05/13/proxying-the-unproxyablex3f-sending-exe-traffic-to-a-proxy-wed-may-13th/
tags:
- veille-cyber
- sans-isc
---
### Analyse du trafic réseau chiffré via Proxifier

L'analyse de flux réseau générés par des exécutables Windows est souvent entravée par l'usage systématique du protocole TLS 1.3, rendant les captures de paquets (PCAP) inexploitables. L'utilisation d'un outil de redirection de trafic permet de contourner cette difficulté en interceptant les requêtes au niveau de l'application.

**Points clés :**
*   **Contournement du chiffrement :** En redirigeant le trafic spécifique d'un exécutable vers un proxy (tel que Burp Suite ou Fiddler), il devient possible de déchiffrer et d'analyser les appels API et les données transmises.
*   **Gestion granulaire :** Proxifier permet de définir des règles de filtrage précises pour isoler le trafic d'un programme cible tout en laissant le reste du système communiquer directement.
*   **Visibilité en temps réel :** L'outil fournit un suivi dynamique des connexions, des journaux d'activité configurables et la capacité d'intercepter et de modifier les requêtes à la volée.

**Vulnérabilités :**
*   Cet article ne traite pas de vulnérabilités spécifiques avec des CVE, mais souligne une limite structurelle de la surveillance réseau classique : l'impossibilité d'inspecter le trafic chiffré TLS 1.3 sans intermédiaire de confiance (proxy) ou capacité d'interception au point de terminaison.

**Recommandations :**
*   **Utilisation d'outils de redirection :** Pour les besoins d'audit ou de rétro-ingénierie, exploitez Proxifier pour forcer le trafic d'exécutables récalcitrants vers un proxy d'inspection.
*   **Configuration des règles :** Il est impératif d'exclure le trafic réseau local (loopback) des règles de proxy pour éviter les interférences avec les processus système standard.
*   **Journalisation :** Activez et configurez la journalisation détaillée dans Proxifier pour faciliter l'analyse post-incident et le suivi des transactions API effectuées par les logiciels inspectés.

---
[Source](https://isc.sans.edu/diary/rss/32982){:target="_blank"}
