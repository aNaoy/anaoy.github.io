---
title: 'Ransomware gangs turn to Shanya EXE packer to hide EDR killers'
date: 2025-12-09
permalink: /posts/2025/12/09/ransomware-gangs-turn-to-shanya-exe-packer-to-hide-edr-killers/
tags:
- veille-cyber
- bleepingcomp
---
### L'obscurité de Shanya : l'outil de dissimulation des gangs de ransomware

Des groupes de ransomware utilisent de plus en plus la plateforme de services "packer" nommée Shanya pour masquer des outils de neutralisation des solutions de détection et de réponse des points d'extrémité (EDR). Shanya propose des outils pour obfusquer le code malveillant, rendant les charges utiles difficiles à détecter par les logiciels de sécurité. Apparu fin 2024, ce service gagne en popularité et a été observé dans plusieurs pays. Les groupes de ransomware comme Medusa, Qilin, Crytox et Akira figurent parmi ses utilisateurs connus, Akira étant le plus assidu.

**Fonctionnement de Shanya :**
Le service prend les charges utiles malveillantes des acteurs de la menace et les "packe" avec un wrapper personnalisé, combinant chiffrement et compression. Chaque client reçoit une version unique du wrapper avec un algorithme de chiffrement spécifique. Le code malveillant est ensuite intégré dans une copie en mémoire du fichier DLL de Windows "shell32.dll". Le payload est déchiffré et décompressé entièrement en mémoire, sans jamais toucher le disque. Shanya inclut des mécanismes pour détecter les EDR en tentant d'appeler une fonction spécifique dans un contexte invalide, ce qui provoque un crash lors d'une analyse par débogueur et interrompt le processus avant l'exécution complète.

**Désactivation des EDR :**
Avant les étapes de vol et de chiffrement des données, les groupes de ransomware cherchent à désactiver les EDR. Ceci est généralement réalisé par le biais de "DLL side-loading", où un exécutable Windows légitime est associé à une DLL malveillante packée par Shanya. L'EDR killer dépose deux pilotes : un pilote signé (ThrottleStop.sys) utilisé pour l'escalade de privilèges, et un pilote non signé (hlpdrv.sys) qui désactive les produits de sécurité sur commande. Ce dernier analyse les processus et services en cours d'exécution, les comparant à une liste pré-établie et envoie des commandes pour les désactiver. Au-delà des ransomware, des campagnes de ClickFix ont également utilisé Shanya pour dissimuler le malware CastleRAT.

**Points clés :**
*   Shanya est un service "packer" utilisé par des groupes de ransomware pour dissimuler leurs charges utiles.
*   Il vise à contourner la détection par les solutions de sécurité, notamment les EDR.
*   Le processus implique le chiffrement, la compression et l'intégration dans des fichiers DLL légitimes en mémoire.
*   Shanya intègre des techniques pour détecter et perturber l'analyse par des EDR.
*   Il est utilisé pour déployer des "EDR killers" qui désactivent les logiciels de sécurité sur les systèmes cibles.
*   Des indicateurs de compromission sont disponibles pour les campagnes utilisant Shanya.

**Vulnérabilités :**
L'article ne mentionne pas de vulnérabilités spécifiques avec des identifiants CVE. Cependant, le mécanisme de désactivation des EDR repose sur l'exploitation de failles potentielles dans la manière dont les EDR gèrent les exceptions ou les appels système, ainsi que sur la capacité des pilotes malveillants à interagir avec le noyau du système. La vulnérabilité dans le pilote ThrottleStop.sys (rwdrv.sys) permettant l'écriture arbitraire en mémoire noyau est un exemple de faiblesse exploitée.

**Recommandations :**
*   Maintenir les solutions de sécurité (EDR, antivirus) à jour pour intégrer les dernières signatures et comportements de détection.
*   Surveiller de près les indicateurs de compromission (IoCs) associés à Shanya pour détecter toute activité suspecte.
*   Implémenter des stratégies de sécurité multicouches, incluant la segmentation réseau, le principe du moindre privilège, et des politiques de sécurité strictes sur le chargement des DLL.
*   Renforcer la surveillance des processus suspects et des chargements de pilotes non autorisés.
*   Former le personnel à reconnaître les signes d'une attaque par ransomware et à réagir de manière appropriée.

---
[Source](https://www.bleepingcomputer.com/news/security/ransomware-gangs-turn-to-shanya-exe-packer-to-hide-edr-killers/){:target="_blank"}
