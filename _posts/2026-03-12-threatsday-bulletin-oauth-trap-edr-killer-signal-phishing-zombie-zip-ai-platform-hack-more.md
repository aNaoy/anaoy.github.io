---
title: 'ThreatsDay Bulletin: OAuth Trap, EDR Killer, Signal Phishing, Zombie ZIP, AI Platform Hack & More'
date: 2026-03-12
permalink: /posts/2026/03/12/threatsday-bulletin-oauth-trap-edr-killer-signal-phishing-zombie-zip-ai-platform-hack-more/
tags:
- veille-cyber
- hackernews
---
### Panorama des menaces : De l'ingénierie sociale aux failles critiques

L'actualité cybersécurité récente révèle une tendance marquée vers des méthodes pragmatiques : détournement de fonctionnalités légitimes, exploitation rapide de vulnérabilités et ingénierie sociale sophistiquée.

#### Points clés
*   **Abus de confiance :** Utilisation croissante de noms de marques légitimes (Adobe, Microsoft) pour des applications OAuth malveillantes et des campagnes de phishing ciblant les identifiants (Signal/WhatsApp, Microsoft Teams via *Quick Assist*).
*   **Évasion et furtivité :** Développement de modules spécialisés comme *BlackSanta* (EDR killer) et de techniques d'obfuscation comme *Zombie ZIP* pour contourner les solutions de défense.
*   **IA et automatisation :** Les agents IA deviennent des vecteurs d'attaque efficaces, capables de compromettre des plateformes internes (ex: McKinsey) en un temps record.
*   **Infrastructures critiques :** Les botnets (ex: *RondoDox*) adoptent des approches "shotgun" en intégrant des exploits dès leur publication, parfois avant même l'assignation d'un CVE.

#### Vulnérabilités notables
*   **CVE-2026-0866 (Zombie ZIP) :** En-têtes ZIP malformés provoquant des faux négatifs dans les outils de sécurité tout en permettant l'extraction du contenu malveillant.
*   **CVE-2025-62593 :** Vulnérabilité critique rapidement intégrée par des réseaux de bots (RondoDox).
*   **Défauts matériels :** Contournement du mot de passe de débogage sur les microcontrôleurs RH850 via injection de fautes en tension (moins d'une minute).

#### Recommandations stratégiques
1.  **Renforcer l'identité :** Privilégier les méthodes d'authentification résistantes au phishing (passkeys, Windows Hello) et auditer régulièrement les applications OAuth autorisées dans le tenant.
2.  **Visibilité accrue :** Activer nativement les fonctionnalités de monitoring (ex: Sysmon sur Windows 11/Server 2025) pour améliorer la détection des comportements anormaux.
3.  **Gestion des accès :** Appliquer le principe du moindre privilège, particulièrement pour les outils d'accès distant et les sessions de support technique (ne jamais autoriser un intervenant non vérifié via *Quick Assist*).
4.  **Défense proactive :** Mettre en place des mécanismes d'inspection des archives et surveiller les flux de données sortants pour détecter les exfiltrations silencieuses exploitant des vulnérabilités logicielles tierces.

---
[Source](https://thehackernews.com/2026/03/threatsday-bulletin-oauth-trap-edr.html){:target="_blank"}
