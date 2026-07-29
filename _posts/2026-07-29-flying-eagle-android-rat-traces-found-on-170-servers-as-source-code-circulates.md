---
title: 'Flying Eagle Android RAT Traces Found on 170 Servers as Source Code Circulates'
date: 2026-07-29
permalink: /posts/2026/07/29/flying-eagle-android-rat-traces-found-on-170-servers-as-source-code-circulates/
tags:
- veille-cyber
- hackernews
---
### Menace Android : Propagation du RAT "Flying Eagle"

Le code source du cheval de Troie d'accès à distance (RAT) pour Android baptisé **Flying Eagle** circule activement sur Telegram. Des chercheurs ont identifié 170 serveurs utilisant ce framework pour orchestrer des campagnes malveillantes, notamment sous couvert d'une fausse application de services publics chinois.

**Points clés :**
* **Distribution :** Le code est diffusé via un pack nommé « Chinese Dragon » contenant l'infrastructure complète (Docker, Nginx, PHP, MySQL, Node.js).
* **Fonctionnalités :** Le malware permet le vol de mots de passe, l'enregistrement d'écran, l'accès à la caméra, la capture de frappes clavier et l'injection de formulaires de phishing.
* **Techniques :** Le builder génère des APK personnalisés en randomisant les noms de paquets, en chiffrant les URL de commande et contrôle (C2) en AES-128-CBC et en utilisant les services d'accessibilité Android pour l'élévation de privilèges et l'injection de gestes.
* **Évolution :** Un nouveau kit nommé **Night Dragon** a également été identifié, démontrant une diversification des outils criminels sur ces canaux.

**Vulnérabilités exploitées :**
* Le malware exploite les **services d'accessibilité d'Android** pour prendre le contrôle total de l'appareil à l'insu de l'utilisateur. 
* *Note : Aucune CVE spécifique n'est mentionnée, le malware utilisant des fonctionnalités légitimes du système Android détournées à des fins malveillantes.*

**Recommandations de sécurité :**
* **Suppression immédiate :** Désinstaller toute application suspecte liée aux services de sécurité cités ou provenant de sources non officielles.
* **Nettoyage :** Effectuer une analyse antivirus complète du terminal mobile.
* **Sécurisation des comptes :** Réinitialiser les mots de passe de tous les comptes accessibles depuis l'appareil compromis.
* **Action financière :** En cas de vol de données, contacter immédiatement les institutions bancaires pour geler les moyens de paiement et signaler l'incident aux autorités compétentes.

---
[Source](https://thehackernews.com/2026/07/flying-eagle-android-rat-traces-found.html){:target="_blank"}
