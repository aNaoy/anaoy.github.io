---
title: 'China-Linked TA4922 Expands Phishing Attacks to U.K., Germany, Italy, and South Africa'
date: 2026-06-04
permalink: /posts/2026/06/04/china-linked-ta4922-expands-phishing-attacks-to-uk-germany-italy-and-south-africa/
tags:
- veille-cyber
- hackernews
---
### Expansion mondiale du groupe cybercriminel TA4922

Le groupe cybercriminel chinois **TA4922**, lié au groupe Silver Fox, intensifie ses activités et étend sa zone d'influence au-delà de l'Asie de l'Est pour cibler désormais des organisations au Royaume-Uni, en Allemagne, en Italie et en Afrique du Sud. Motivé par le gain financier, ce groupe utilise des tactiques sophistiquées pour voler des données, commettre des fraudes ou revendre des accès distants.

**Points clés :**
*   **Mode opératoire :** Utilisation intensive de campagnes de phishing basées sur des thématiques professionnelles (RH, fiscalité, factures, conformité).
*   **Technique de contournement :** Transfert volontaire des communications vers des canaux hors bande (LINE, WhatsApp, Microsoft Teams) pour échapper aux outils de sécurité d'entreprise.
*   **Arsenal logiciel :** Utilisation de familles de malwares connues (ValleyRAT, Atlas RAT) et de nouveaux outils propriétaires (RomulusLoader, SilentRunLoader).
*   **Vecteur d'infection :** Exploitation récurrente du **DLL side-loading** pour exécuter des charges malveillantes.

**Vulnérabilités :**
Bien qu'aucune CVE spécifique ne soit mentionnée, les attaques reposent sur l'exploitation humaine (ingénierie sociale) et sur le détournement de processus légitimes via le **DLL side-loading**, permettant de charger des bibliothèques malveillantes par des applications de confiance.

**Recommandations :**
*   **Sensibilisation :** Former les employés à la méfiance face aux sollicitations professionnelles inattendues, particulièrement celles encourageant une migration vers des messageries privées (WhatsApp, LINE).
*   **Surveillance réseau :** Bloquer ou surveiller étroitement le trafic vers les plateformes de messagerie personnelles dans un contexte professionnel.
*   **Contrôle des applications :** Restreindre les privilèges d'exécution et mettre en œuvre des politiques d'intégrité pour prévenir le DLL side-loading.
*   **Sécurisation des endpoints :** Déployer des solutions EDR capables de détecter des comportements anormaux, comme l'exfiltration de cookies ou de données de navigateurs par des processus non autorisés (notamment via SilentRunLoader).

---
[Source](https://thehackernews.com/2026/06/china-linked-ta4922-expands-phishing.html){:target="_blank"}
