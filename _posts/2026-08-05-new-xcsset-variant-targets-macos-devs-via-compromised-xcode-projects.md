---
title: 'New XCSSET variant targets macOS devs via compromised Xcode projects'
date: 2026-08-05
permalink: /posts/2026/08/05/new-xcsset-variant-targets-macos-devs-via-compromised-xcode-projects/
tags:
- veille-cyber
- bleepingcomp
---
### Recrudescence du malware XCSSET ciblant les développeurs macOS

Une nouvelle version (v40) du malware XCSSET sévit sur macOS en infiltrant des projets Xcode légitimes via des dépôts GitHub compromis. Une fois qu'un développeur compile le projet infecté, le malware se propage à l'ensemble des projets Xcode du système et déploie 17 modules malveillants.

**Points clés :**
* **Infection :** Le malware utilise des scripts téléchargeurs dissimulés dans des projets Xcode. Une fois actif, il s'auto-réplique via le code source partagé.
* **Nouvelles fonctionnalités :**
    * **Hijacker Chrome :** Intercepte le trafic web, les identifiants, les cookies et les transactions de cryptomonnaies (MetaMask) en détournant les paiements.
    * **Trojanisation de Telegram :** Remplace l'application Telegram officielle par une version malveillante pour intercepter les communications.
* **Évasion :** Utilise le chiffrement dynamique des communications, l'obfuscation de code et la re-compilation périodique du chargeur pour échapper à la détection.
* **Auto-défense :** Le malware tente activement de désactiver les mécanismes de sécurité de macOS (XProtect, MRT, TCC, Rapid Security Response) et bloque les mises à jour des signatures de sécurité.

**Vulnérabilités :**
* Aucune CVE spécifique n'est mentionnée pour cette variante, bien que le malware soit connu pour exploiter historiquement des vulnérabilités de type "zero-day" pour compromettre la sécurité du système macOS.

**Recommandations :**
* **Audit des dépendances :** Scanner systématiquement les projets open-source et les dépendances avant de les intégrer dans les pipelines de développement.
* **Surveillance proactive :** Porter une attention particulière aux activités AppleScript anormales, aux modifications non autorisées des navigateurs et à la création de domaines par défaut suspects dans macOS.
* **Détection Gatekeeper :** Surveiller l'exécution d'applications signées de manière "ad hoc" qui tentent de contourner les protections natives Gatekeeper.

---
[Source](https://www.bleepingcomputer.com/news/security/new-xcsset-variant-targets-macos-devs-via-compromised-xcode-projects/){:target="_blank"}
