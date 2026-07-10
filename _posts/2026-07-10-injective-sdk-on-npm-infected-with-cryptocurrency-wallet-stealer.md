---
title: 'Injective SDK on npm infected with cryptocurrency wallet stealer'
date: 2026-07-10
permalink: /posts/2026/07/10/injective-sdk-on-npm-infected-with-cryptocurrency-wallet-stealer/
tags:
- veille-cyber
- bleepingcomp
---
### Compromission de la supply-chain : Le SDK Injective détourné

Le dépôt GitHub du SDK Injective Labs a été compromis via un compte contributeur légitime, permettant aux attaquants de publier la version malveillante **1.20.21** du paquet npm `@injectivelabs/sdk-ts`. Cette attaque par chaîne d'approvisionnement a également impacté 17 autres paquets dépendants. Bien que le correctif (version 1.20.23) ait été publié rapidement, le code malveillant a été téléchargé 310 fois avant d'être écarté.

**Points clés :**
*   **Mécanisme d'infection :** Le malware ne s'active pas à l'installation, mais lors de l'appel aux fonctions de génération ou d'importation de clés de portefeuille.
*   **Exfiltration :** Les phrases mnémoniques et clés privées sont encodées en base64, puis exfiltrées via des requêtes HTTP POST dissimulées vers une infrastructure publique d'Injective pour paraître légitimes.
*   **Impact :** Environ 112 000 téléchargements cumulés pour les 87 paquets dépendants du SDK.
*   **Vulnérabilité :** Aucune CVE spécifique n'a été assignée, il s'agit d'une compromission de compte GitHub (Supply Chain Attack) menant à l'injection de code malveillant dans un paquet officiel.

**Recommandations :**
*   **Audit immédiat :** Si vous avez utilisé la version 1.20.21, considérez votre environnement de développement comme compromis.
*   **Rotation des secrets :** Transférez immédiatement tous les actifs numériques vers de nouveaux portefeuilles sécurisés et invalidez toutes les clés privées et phrases mnémoniques potentiellement exposées.
*   **Mise à jour :** Assurez-vous d'utiliser exclusivement la version propre (1.20.23 ou supérieure) du SDK.
*   **Sécurisation :** Implémentez des outils de surveillance de la chaîne d'approvisionnement logicielle pour détecter les changements suspects dans les dépendances.

---
[Source](https://www.bleepingcomputer.com/news/security/injective-sdk-on-npm-infected-with-cryptocurrency-wallet-stealer/){:target="_blank"}
