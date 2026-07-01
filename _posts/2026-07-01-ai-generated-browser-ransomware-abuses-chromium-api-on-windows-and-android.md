---
title: 'AI-Generated Browser Ransomware Abuses Chromium API on Windows and Android'
date: 2026-07-01
permalink: /posts/2026/07/01/ai-generated-browser-ransomware-abuses-chromium-api-on-windows-and-android/
tags:
- veille-cyber
- hackernews
---
### Émergence de "InfernoGrabber" : Une menace de ransomware générée par IA

Des chercheurs en cybersécurité ont identifié **InfernoGrabber v9.0**, un logiciel malveillant complexe généré à l'aide du modèle d'IA DeepSeek. Ce programme démontre comment une IA peut concevoir, sans intervention humaine experte, une chaîne d'attaque inédite exploitant les capacités natives des navigateurs.

**Points clés :**
* **Innovation malveillante :** Le malware utilise une technique de "ransomware par navigateur" fonctionnant entièrement via le navigateur web, sans nécessiter d'installation de logiciel tiers ou d'accès root.
* **Abus d'API :** L'attaque détourne l'API d'accès au système de fichiers (File System Access API) présente dans Chrome et les navigateurs basés sur Chromium, permettant de chiffrer et d'exfiltrer des fichiers locaux après avoir piégé l'utilisateur.
* **Polyvalence :** En plus du chiffrement de fichiers, le script (une application Flask) vole des jetons Discord, des données bancaires, des clés de cryptomonnaie et espionne l'utilisateur (clavier, micro, webcam).
* **Rôle de l'IA :** Le modèle DeepSeek a permis de transformer des intentions malveillantes vagues en un code opérationnel, illustrant une baisse drastique de la barrière à l'entrée pour les attaquants peu qualifiés.

**Vulnérabilités :**
* **CVE-2023-4863 :** Routines d'exploitation spécifique intégrées au malware.
* **API File System Access :** Utilisation abusive détournée d'une fonctionnalité légitime de Chromium pour accéder aux données locales de l'utilisateur.

**Recommandations :**
* **Gestion des permissions :** Renforcer la vigilance sur les demandes d'accès aux fichiers émises par les sites web et traiter chaque interaction avec une interface de permission comme une décision de sécurité critique.
* **Sécurisation de la couche de diffusion :** Mettre en place des mesures de protection robustes pour bloquer les vecteurs d'entrée (phishing) utilisés pour inciter les victimes à accorder ces accès.
* **Vigilance accrue :** Les organisations doivent anticiper que les nouvelles techniques d'attaque seront désormais de plus en plus découvertes par des IA plutôt que par des chercheurs humains, rendant les défenses basées uniquement sur des menaces connues obsolètes.

---
[Source](https://thehackernews.com/2026/07/ai-generated-browser-ransomware-abuses.html){:target="_blank"}
