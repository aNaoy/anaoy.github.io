---
title: 'Free real estate: GoPix, the banking Trojan living off your memory'
date: 2026-03-16
permalink: /posts/2026/03/16/free-real-estate-gopix-the-banking-trojan-living-off-your-memory/
tags:
- veille-cyber
- securelist
---
# GoPix : Le cheval de Troie bancaire brésilien invisible

GoPix est un cheval de Troie bancaire sophistiqué ciblant les institutions financières et les utilisateurs de cryptomonnaies au Brésil. Ce malware se distingue par son fonctionnement "sans fichier" (fileless) et son exécution uniquement en mémoire, exploitant des techniques avancées pour échapper aux outils de détection et d'investigation numérique.

### Points clés
*   **Vecteur d'infection :** Utilisation de publicités malveillantes (malvertising) sur Google Ads redirigeant vers des pages de téléchargement frauduleuses.
*   **Filtrage des victimes :** Le malware utilise des services anti-fraude légitimes pour identifier les cibles de valeur et éviter les environnements de sandbox ou les chercheurs en cybersécurité.
*   **Techniques d'évasion :** Utilisation de LOLBins (Living-off-the-Land Binaries), de scripts PowerShell obfusqués et de certificats de signature de code volés.
*   **Persistance furtive :** Les modules malveillants sont chargés directement en mémoire, ne laissant quasiment aucune trace sur le disque. Le malware utilise des serveurs de commande et de contrôle (C2) à très courte durée de vie.
*   **Attaque Man-in-the-Middle (MitM) :** Manipulation du trafic via des fichiers PAC (Proxy AutoConfig) et injection d'un certificat racine de confiance dans le navigateur pour intercepter les flux HTTPS.

### Capacités malveillantes
*   **Surveillance du presse-papiers :** Détection et interception des transactions Pix et Boleto bancário.
*   **Vol de cryptomonnaies :** Remplacement automatique des adresses de portefeuilles Bitcoin/Ethereum par celles des attaquants lors d'un copier-coller.
*   **Architecture modulaire :** Capacité à basculer entre les processus pour maximiser la discrétion et contourner les logiciels de sécurité.

### Vulnérabilités exploitées
Bien qu'aucune CVE spécifique ne soit citée (le malware s'appuie sur une exécution légitime de PowerShell et de binaires système), l'attaque exploite :
*   Le mécanisme des fichiers **PAC** pour le détournement de trafic.
*   La confiance accordée aux **certificats racine** installés manuellement dans le magasin du navigateur.
*   L'usage détourné de fonctionnalités de **browser security** (comme le port 27275 lié à Avast Safe Banking).

### Recommandations
*   **Filtrage publicitaire :** Sensibiliser les utilisateurs aux risques liés aux publicités sur les moteurs de recherche et encourager l'utilisation de bloqueurs de publicités ou de navigateurs sécurisés.
*   **Surveillance du réseau :** Surveiller les requêtes inhabituelles vers des fichiers `.pac` et inspecter les certificats racines installés manuellement dans les navigateurs.
*   **Politiques PowerShell :** Restreindre l'exécution de scripts PowerShell (via Constrained Language Mode) pour limiter l'impact des attaques par injection mémoire.
*   **Gestion des certificats :** Auditer régulièrement les autorités de certification racines de confiance sur les postes de travail des employés.
*   **Protection des endpoints :** Utiliser des solutions EDR capables de détecter les comportements anormaux en mémoire et les injections de code, plutôt que de se baser uniquement sur les signatures de fichiers.

---
[Source](https://securelist.com/gopix-banking-trojan/119173/){:target="_blank"}
