---
title: '.NET SOAPwn Flaw Opens Door for File Writes and Remote Code Execution via Rogue WSDL'
date: 2025-12-11
permalink: /posts/2025/12/11/net-soapwn-flaw-opens-door-for-file-writes-and-remote-code-execution-via-rogue-wsdl/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité SOAPwn dans le Framework .NET

Une faille de sécurité, baptisée SOAPwn, a été découverte dans le framework .NET, ouvrant la porte à l'écriture de fichiers arbitraires et à l'exécution de code à distance via des descriptions de services web (WSDL) malveillantes.

Cette vulnérabilité exploite la manière dont les applications .NET gèrent les messages SOAP et interagissent avec les proxys HTTP client. En manipulant le WSDL utilisé par un client SOAP, un attaquant peut rediriger les requêtes SOAP vers des fichiers locaux au lieu de les envoyer via HTTP. Cela permet d'écrire du contenu contrôlé dans des fichiers, potentiellement en écrasant des fichiers existants, et d'obtenir l'exécution de code à distance. Les vecteurs d'attaque incluent l'utilisation de chemins de type "file://..." pour écrire sur le système de fichiers, ou l'injection d'un WSDL malveillant pour que l'application génère un proxy HTTP client qui télécharge un webshell (comme ASPX ou CSHTML) ou des scripts PowerShell.

Cette faille a été observée dans des produits tels que Barracuda Service Center RMM, Ivanti Endpoint Manager (EPM) et Umbraco 8.

**Points Clés :**

*   La vulnérabilité SOAPwn affecte le framework .NET.
*   Elle permet l'écriture de fichiers arbitraires et l'exécution de code à distance.
*   L'exploitation repose sur l'abus des descriptions de services web (WSDL) et des proxys HTTP client.
*   Microsoft considère qu'il s'agit d'un problème lié à la consommation d'entrées non fiables par les applications.

**Vulnérabilités :**

*   **CVE-2025-34392** (Barracuda Service Center RMM version 2025.1.1, CVSS 9.8)
*   **CVE-2025-13659** (Ivanti EPM version 2024 SU4 SR1, CVSS 8.8)
*   Umbraco 8 est affecté, mais a atteint sa fin de vie (EoL) le 24 février 2025.

**Recommandations :**

*   Pour les utilisateurs de Barracuda Service Center RMM, assurez-vous d'être sur la version 2025.1.1 ou supérieure.
*   Pour les utilisateurs d'Ivanti Endpoint Manager (EPM), appliquez la version 2024 SU4 SR1 ou ultérieure.
*   Pour Umbraco 8, une mise à jour n'est pas disponible en raison de la fin de vie du produit. Il est fortement recommandé de migrer vers une version supportée d'Umbraco ou un autre CMS.
*   Les développeurs d'applications .NET doivent être vigilants quant à la validation des entrées provenant de sources non fiables, en particulier lors de l'importation ou de la génération de proxys à partir de WSDL.

---
[Source](https://thehackernews.com/2025/12/net-soapwn-flaw-opens-door-for-file.html){:target="_blank"}
