---
title: 'WebRTC Skimmer Bypasses CSP to Steal Payment Data from E-Commerce Sites'
date: 2026-03-26
permalink: /posts/2026/03/26/webrtc-skimmer-bypasses-csp-to-steal-payment-data-from-e-commerce-sites/
tags:
- veille-cyber
- hackernews
---
### Évolution des skimmers e-commerce : contournement des CSP via WebRTC

Une nouvelle campagne de piratage de données bancaires cible les sites e-commerce utilisant Magento et Adobe Commerce. Cette attaque se distingue par l'utilisation du protocole WebRTC pour exfiltrer les données, rendant les mécanismes de défense traditionnels inefficaces.

**Points clés :**
*   **Technique d'exfiltration :** Le malware utilise des canaux de données WebRTC (chiffrés DTLS sur UDP) pour charger des scripts malveillants et envoyer les informations volées.
*   **Contournement de sécurité :** Cette méthode permet de contourner les politiques de sécurité de contenu (CSP) et les outils de surveillance réseau qui inspectent uniquement le trafic HTTP.
*   **Vecteur d'infection :** L'attaque repose sur **PolyShell**, une vulnérabilité permettant le téléchargement de fichiers arbitraires via l'API REST de Magento, menant à une exécution de code à distance (RCE).
*   **Exploitation massive :** Plus de 50 adresses IP distinctes participent activement à l'exploitation de cette faille sur les boutiques en ligne.

**Vulnérabilités :**
*   **PolyShell :** Vulnérabilité de téléversement de fichiers non authentifié dans `ImageProcessor::processImageContent()`. Elle permet de contourner les vérifications d'extension de fichier, facilitant l'exécution de code si la configuration du serveur web (Nginx/Apache) est incomplète.

**Recommandations :**
*   **Correction logicielle :** Mettre à jour vers les versions sécurisées dès leur disponibilité (Adobe Commerce 2.4.9-beta1 inclut des correctifs).
*   **Durcissement du serveur :** Bloquer strictement l'accès au répertoire `pub/media/custom_options/` et s'assurer que les fichiers PHP ne peuvent pas y être exécutés.
*   **Audit de sécurité :** Rechercher la présence de web shells, de portes dérobées et de tout script non autorisé sur le serveur.
*   **Configuration :** Appliquer rigoureusement les configurations Nginx/Apache recommandées par Adobe pour restreindre l'exécution de fichiers dans les dossiers médias.

---
[Source](https://thehackernews.com/2026/03/webrtc-skimmer-bypasses-csp-to-steal.html){:target="_blank"}
