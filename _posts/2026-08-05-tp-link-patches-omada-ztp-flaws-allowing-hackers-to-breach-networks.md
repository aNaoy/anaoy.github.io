---
title: 'TP-Link patches Omada ZTP flaws allowing hackers to breach networks'
date: 2026-08-05
permalink: /posts/2026/08/05/tp-link-patches-omada-ztp-flaws-allowing-hackers-to-breach-networks/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilités critiques dans le mécanisme ZTP de TP-Link Omada

TP-Link a corrigé 15 vulnérabilités majeures au sein de son mécanisme de déploiement « Zero-Touch Provisioning » (ZTP) affectant la gamme professionnelle Omada (routeurs, points d'accès, switchs). L'exploitation en chaîne de ces failles, combinée à des vulnérabilités d'injection de commandes préexistantes, permet à un attaquant distant de prendre le contrôle total des équipements et d'infiltrer les réseaux internes.

**Points clés :**
*   **Surface d'attaque étendue :** Les failles touchent les contrôleurs, passerelles, applications mobiles et services cloud de TP-Link.
*   **Vecteurs d'attaque :** Les attaquants peuvent usurper l'identité de dispositifs, exploiter des conditions de compétition (« race conditions ») lors de l'adoption cloud, et récupérer des identifiants (hachages MD5, clés VPN) en clair.
*   **Risques :** Exécution de code à distance (RCE), vol d'identifiants administrateur via injection JavaScript (phishing), et création de tunnels VPN non autorisés.

**Vulnérabilités identifiées (CVE) :**
*   CVE-2025-9289 à CVE-2025-9293
*   CVE-2025-15544
*   CVE-2025-15627 à CVE-2025-15631
*   *Note : 4 vulnérabilités supplémentaires sans identifiant CVE (liées aux numéros de série prévisibles, aux identifiants par défaut et aux liens de téléchargement non authentifiés).*
*   *CVE associées aux exploits en chaîne : CVE-2025-7850 et CVE-2025-7851.*

**Recommandations :**
*   **Mise à jour :** Installer immédiatement les derniers firmwares disponibles sur le portail officiel de TP-Link.
*   **Sécurisation des accès :** Utiliser des mots de passe administrateur robustes et uniques.
*   **Authentification :** Activer systématiquement l'authentification multifacteur (MFA).
*   **Hygiène réseau :** Surveiller le trafic réseau pour détecter toute activité suspecte et éviter l'exposition directe des contrôleurs Omada sur Internet.
*   **Maintenance :** Mettre à jour toutes les applications mobiles liées (Omada/Omada Guard) et procéder à une rotation des secrets (clés VPN, mots de passe) en cas de suspicion de compromission.

---
[Source](https://www.bleepingcomputer.com/news/security/tp-link-patches-omada-ztp-flaws-allowing-hackers-to-breach-networks/){:target="_blank"}
