---
title: 'Evasive Panda APT poisons DNS requests to deliver MgBot'
date: 2025-12-24
permalink: /posts/2025/12/24/evasive-panda-apt-poisons-dns-requests-to-deliver-mgbot/
tags:
- veille-cyber
- securelist
---
**Evasive Panda : Une nouvelle campagne utilise le DNS empoisonné pour déployer MgBot**

Le groupe de menace persistante avancée (APT) Evasive Panda, actif depuis 2012, a mené des campagnes très ciblées entre novembre 2022 et novembre 2024. Ces attaques visaient des industries spécifiques, employant notamment des techniques d'attaques par l'homme du milieu (AitM). Les opérateurs ont développé un nouveau chargeur pour contourner la détection et utilisent le malware MgBot, injecté dans des processus légitimes pour maintenir une présence discrète.

**Points Clés :**

*   **Ciblage :** Campagnes hautement ciblées visant des victimes spécifiques.
*   **Méthodologie :** Utilisation de leurres tels que de fausses mises à jour d'applications populaires (SohuVA, iQIYI, IObit Smart Defrag, Tencent QQ) pour délivrer le malware.
*   **Techniques Avancées :**
    *   Chargement en mémoire par injection dans des processus légitimes (DLL sideloading).
    *   Chiffrement hybride (DPAPI + RC5) pour rendre l'analyse du malware plus complexe et unique par victime.
    *   Utilisation d'un chargeur développé en C++ avec le Windows Template Library (WTL).
    *   Résolution discrète des API Windows à l'aide d'un algorithme de hachage PJW.
*   **Persistance :** Certaines victimes sont compromises depuis plus d'un an, indiquant une capacité de maintien à long terme.
*   **Attribution :** Les TTP observés sont fortement attribués à Evasive Panda.

**Vulnérabilités et Mécanismes Exploités :**

*   **DNS Poisoning :** Une technique clé utilisée pour rediriger les requêtes DNS de sites légitimes (ex: `dictionary.com`) vers des serveurs contrôlés par l'attaquant, afin de récupérer des composants du malware. La méthode exacte pour réaliser cet empoisonnement ciblé sur les FAI ou les appareils réseau des victimes reste incertaine.
*   **Confusion des Fichiers :** Utilisation de noms de fichiers ressemblant à des exécutables ou des bibliothèques légitimes (ex: `sohuva_update_10.2.29.1-lup-s-tp.exe`, `libpython2.4.dll`).
*   **Injection de Code :** Injection de shellcode et du malware final MgBot dans des processus légitimes comme `svchost.exe`.

**Recommandations :**

Bien que l'article ne contienne pas de section dédiée aux recommandations de sécurité, les techniques utilisées par Evasive Panda suggèrent la nécessité de :

*   **Surveillance du trafic réseau :** Détecter les anomalies dans les requêtes DNS et les connexions sortantes vers des adresses IP suspectes.
*   **Analyse comportementale des processus :** Identifier les injections de code et l'exécution de processus inhabituels.
*   **Mise à jour des logiciels :** Maintenir à jour les applications et les systèmes d'exploitation pour corriger les vulnérabilités potentielles.
*   **Sensibilisation des utilisateurs :** Éduquer les employés sur les risques liés aux téléchargements et aux mises à jour provenant de sources non fiables.
*   **Contrôle d'accès réseau :** Sécuriser les routeurs et les pare-feux pour prévenir les compromissions au niveau du réseau qui pourraient faciliter le DNS poisoning.

**Indicateurs de Compromission :**

*   **Hashes de Fichiers :**
    *   `c340195696d13642ecf20fbe75461bed` (sohuva_update_10.2.29.1-lup-s-tp.exe)
    *   `7973e0694ab6545a044a49ff101d412a` (libpython2.4.dll)
    *   `9e72410d61eaa4f24e0719b34d7cad19` (Implant MgBot)
*   **Chemins de Fichiers :**
    *   `C:\ProgramData\Microsoft\MF`
    *   `C:\ProgramData\Microsoft\eHome\status.dat`
    *   `C:\ProgramData\Microsoft\eHome\perf.dat`
*   **URLs et IPs (exemples) :**
    *   `60.28.124[.]21` (MgBot C2)
    *   `103.96.130[.]107` (AitM C2)
    *   `158.247.214[.]28` (AitM C2)

---
[Source](https://securelist.com/evasive-panda-apt/118576/){:target="_blank"}
