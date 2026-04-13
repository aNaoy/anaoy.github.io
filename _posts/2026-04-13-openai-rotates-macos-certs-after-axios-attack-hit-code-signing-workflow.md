---
title: 'OpenAI rotates macOS certs after Axios attack hit code-signing workflow'
date: 2026-04-13
permalink: /posts/2026/04/13/openai-rotates-macos-certs-after-axios-attack-hit-code-signing-workflow/
tags:
- veille-cyber
- bleepingcomp
---
### Compromission de la chaîne d'approvisionnement Axios chez OpenAI

OpenAI a été victime d'une attaque par chaîne d'approvisionnement le 31 mars 2026, impliquant une version malveillante du paquet npm `Axios` (v1.14.1). Exécuté via un workflow GitHub Actions, ce code malveillant a potentiellement exposé les certificats de signature de code des applications macOS de l'entreprise.

**Points clés :**
*   **Origine :** Les attaquants (groupe UNC1069) ont compromis le compte d'un mainteneur du projet Axios via une campagne d'ingénierie sociale sophistiquée (fausses réunions Teams/Slack).
*   **Impact :** Bien qu'aucune preuve d'altération des logiciels ou de vol de données n'ait été détectée, OpenAI a décidé par précaution de révoquer ses certificats de signature macOS.
*   **Périmètre :** Seules les applications macOS (ChatGPT Desktop, Codex, Codex CLI et Atlas) sont concernées. Les services web, iOS, Android, Windows, Linux, ainsi que les comptes utilisateurs et clés API, restent sécurisés.

**Vulnérabilités :**
*   **Supply Chain Attack :** Utilisation d'un paquet npm compromis (`Axios` v1.14.1) dans un environnement CI/CD (GitHub Actions).
*   **CVE :** Aucune CVE spécifique n'est mentionnée pour cette attaque de chaîne d'approvisionnement, celle-ci reposant sur l'injection de code malveillant dans un dépôt légitime via le compte d'un mainteneur compromis.

**Recommandations :**
*   **Mise à jour immédiate :** Tous les utilisateurs macOS doivent mettre à jour leurs applications OpenAI vers les dernières versions signées avec le nouveau certificat.
*   **Obsolescence :** Les anciennes versions des applications cesseront de fonctionner à partir du 8 mai 2026 suite à la révocation définitive du certificat.
*   **Vigilance :** Téléchargez exclusivement les logiciels via les sites officiels ou les outils internes intégrés. Évitez toute installation provenant de liens suspects reçus par e-mail ou publicités.

---
[Source](https://www.bleepingcomputer.com/news/security/openai-rotates-macos-certs-after-axios-attack-hit-code-signing-workflow/){:target="_blank"}
