---
title: 'Kimsuky targets organizations with PebbleDash-based tools'
date: 2026-05-14
permalink: /posts/2026/05/14/kimsuky-targets-organizations-with-pebbledash-based-tools/
tags:
- veille-cyber
- securelist
---
# Évolution tactique du groupe APT Kimsuky : focus sur PebbleDash

Le groupe cybercriminel Kimsuky (également connu sous les noms d'APT43 ou Ruby Sleet) intensifie ses activités avec des outils sophistiqués basés sur la plateforme **PebbleDash**. Le groupe démontre une capacité d'adaptation constante, intégrant désormais des LLM pour générer des commentaires de code, le langage Rust, et le détournement de services légitimes pour ses campagnes d'espionnage.

### Points clés
*   **Ciblage :** Principalement les secteurs public, privé et de la défense en Corée du Sud, avec des extensions vers le Brésil et l'Allemagne.
*   **Vecteur d'accès :** Campagnes de spear-phishing (via e-mail ou messagerie) utilisant des fichiers joints piégés (JSE, PIF, SCR, EXE) déguisés en documents administratifs ou offres d'emploi.
*   **Outils de post-exploitation :** Détournement des fonctionnalités de tunneling de **Visual Studio Code** et déploiement de l'outil de gestion à distance **DWAgent** pour maintenir un accès persistant tout en contournant les détections classiques.
*   **Diversification technologique :** Utilisation de variantes en Rust (HelloDoor) et recours fréquent à des services comme Cloudflare Quick Tunnels ou des sites web légitimes compromis pour héberger leur infrastructure de commande et contrôle (C2).

### Vulnérabilités et vecteurs d'attaque
L'article ne mentionne pas de CVE spécifique exploitant des failles logicielles de type "Zero-day", mais souligne l'abus de fonctionnalités légitimes (Living off the Land) :
*   **Détournement de VSCode :** L'usage abusif de `code tunnel` permet de créer des accès distants authentifiés via GitHub.
*   **Abus de services tiers :** Utilisation détournée de DWAgent, Dropbox, et des services de tunneling Cloudflare pour masquer le trafic malveillant.
*   **Manipulation de certificats :** Vol de certificats numériques sud-coréens (dont ceux du GPKI) pour signer des malwares et éviter les alertes de sécurité.

### Recommandations de sécurité
*   **Filtrage des e-mails :** Renforcer la détection des extensions de fichiers suspectes (.JSE, .PIF, .SCR) et sensibiliser les employés aux techniques d'ingénierie sociale basées sur des documents administratifs factices.
*   **Contrôle des applications :** Restreindre l'exécution des outils de tunneling (VSCode CLI, DWAgent) via des politiques de contrôle d'application (AppLocker ou solutions EDR).
*   **Surveillance réseau :** Détecter les connexions inhabituelles vers des domaines éphémères (ex: `trycloudflare.com`) ou des services de tunneling non autorisés au sein du réseau d'entreprise.
*   **Gestion des identités :** Appliquer le principe du moindre privilège et surveiller étroitement les accès GitHub ou Microsoft utilisés pour la gestion des infrastructures distantes.
*   **Audits de configuration :** Vérifier régulièrement les clés de registre de persistance (`HKCU\...\Run`) et la création de tâches planifiées suspectes associées aux noms mentionnés dans l'article (ex: `ChromeCheck`, `EdgeCheck`, `CacheDB`).

---
[Source](https://securelist.com/kimsuky-appleseed-pebbledash-campaigns/119785/){:target="_blank"}
