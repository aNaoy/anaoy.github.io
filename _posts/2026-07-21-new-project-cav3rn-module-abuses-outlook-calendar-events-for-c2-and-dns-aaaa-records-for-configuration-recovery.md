---
title: 'New Project CAV3RN module abuses Outlook calendar events for C2 and DNS AAAA records for configuration recovery'
date: 2026-07-21
permalink: /posts/2026/07/21/new-project-cav3rn-module-abuses-outlook-calendar-events-for-c2-and-dns-aaaa-records-for-configuration-recovery/
tags:
- veille-cyber
- securelist
---
### Analyse du module de communication de Project CAV3RN : Utilisation détournée de Microsoft Graph et DNS

Le framework d'espionnage cybernétique **Project CAV3RN** a évolué avec l'introduction d'un nouveau module de communication (`AzureCommunication.dll`), conçu pour remplacer les composants HTTP/WebSocket précédents. Ce module utilise les services Microsoft 365 pour piloter ses opérations tout en intégrant un mécanisme de secours basé sur le protocole DNS.

#### Points clés
*   **C2 via Outlook :** Le module utilise l'API **Microsoft Graph** pour transformer le calendrier Outlook d'une boîte mail compromise en canal de commande et de contrôle (C2).
*   **Fonctionnement :** Les attaquants créent des événements de calendrier (fixés à l'année 2050 pour éviter d'être remarqués) contenant des pièces jointes chiffrées (RSA + AES-GCM) pour transmettre les commandes et récupérer les données exfiltrées.
*   **Architecture modulaire :** Le module est compilé en .NET Native AOT, rendant l'analyse statique complexe. Il interagit avec un contrôleur central via une interface d'export unique (`QueryInterface`).
*   **Mécanisme de secours (DNS) :** En cas d'échec d'authentification sur Microsoft Graph, le malware utilise des requêtes **DNS AAAA** personnalisées vers un domaine contrôlé par les attaquants (`cloudlanecdn[.]com`) pour récupérer de nouvelles configurations (Tenant ID, Client ID, etc.).
*   **Attribution :** Les tactiques, techniques et procédures (TTP) observées renforcent l'hypothèse d'un lien avec le groupe **OilRig (APT34)**, bien que l'attribution demeure à "faible confiance" en l'absence de preuve matérielle directe.

#### Vulnérabilités et vecteurs d'attaque
*   **Détournement d'API légitimes :** Le malware abuse des API Microsoft Graph et de l'infrastructure de calendrier pour masquer ses activités sous un trafic légitime.
*   **Exfiltration par DNS :** Utilisation du protocole DNS comme canal de communication secondaire pour contourner les mesures de sécurité réseau traditionnelles (les données sont encodées dans les adresses IPv6 retournées par les requêtes AAAA).
*   *Note : Aucune CVE spécifique n'est mentionnée, car l'attaque repose sur une utilisation détournée (abus de fonctionnalité) et non sur l'exploitation d'une faille logicielle connue.*

#### Recommandations
*   **Surveillance des logs Microsoft 365 :** Surveiller les accès suspects via Microsoft Graph, particulièrement les requêtes de lecture/écriture sur les calendriers qui ne correspondent pas à une activité utilisateur normale.
*   **Analyse du trafic DNS :** Détecter les requêtes DNS inhabituelles vers des domaines inconnus ou les réponses AAAA dont la structure est atypique (ex: encodage de données dans les segments IPv6).
*   **Détection d'anomalies :** Repérer la création d'événements de calendrier avec des dates lointaines (ex: 2050) ou des sujets utilisant des formats suspects (ID d'agent, "Boss Update", etc.).
*   **Sécurisation des accès API :** Appliquer le principe du moindre privilège aux applications inscrites dans Entra ID et restreindre les autorisations Microsoft Graph aux seules fonctionnalités réellement nécessaires à l'entreprise.

---
[Source](https://securelist.com/project-cav3rn-cyberespionage-framework-using-outlook-and-dns/120757/){:target="_blank"}
