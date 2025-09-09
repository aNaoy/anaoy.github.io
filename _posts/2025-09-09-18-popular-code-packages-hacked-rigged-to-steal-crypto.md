---
title: '18 Popular Code Packages Hacked, Rigged to Steal Crypto'
date: 2025-09-09
permalink: /posts/2025/09/09/18-popular-code-packages-hacked-rigged-to-steal-crypto/
tags:
- veille-cyber
- krebs
---
**Compromission de paquets de code JavaScript : Vol de cryptomonnaies et risques de sécurité accrus**

Dix-huit paquets de code JavaScript populaires, totalisant plus de deux milliards de téléchargements hebdomadaires, ont été brièvement compromis par un logiciel malveillant. L'incident, qui visait spécifiquement le vol de cryptomonnaies, a été rendu possible par une attaque de phishing ciblant un développeur clé. Ce dernier, dupé par un faux site de connexion NPM demandant la mise à jour de son authentification à deux facteurs (2FA), a vu ses identifiants et son jeton 2FA dérobés. Les attaquants ont ensuite utilisé son compte NPM pour injecter du code malveillant dans plusieurs bibliothèques JavaScript largement utilisées.

Ce code malveillant agissait comme un intercepteur basé sur le navigateur, capable de voler le trafic réseau et de manipuler les appels API. Il interceptait les activités liées aux cryptomonnaies, redirigeant les fonds et les approbations vers des comptes contrôlés par les attaquants, le tout sans éveiller les soupçons de l'utilisateur.

Les experts soulignent la gravité potentielle de telles attaques de chaîne d'approvisionnement. Bien que cet incident ait été rapidement contenu et limité au vol de cryptomonnaies, une charge utile plus néfaste aurait pu entraîner une épidémie de logiciels malveillants difficile à détecter et à maîtriser. L'incident met en lumière la fragilité de l'écosystème logiciel moderne, où la sécurité repose souvent sur un petit nombre de développeurs surchargés et sous-ressourcés.

**Points Clés :**

*   **Attaque de Phishing Ciblée :** Un développeur a été victime d'une attaque de phishing imitant la page de connexion NPM, entraînant le vol de ses identifiants et de son jeton 2FA.
*   **Compromission de Paquets Populaires :** Au moins 18 bibliothèques JavaScript largement utilisées via NPM ont été infectées par du code malveillant.
*   **Vol de Cryptomonnaies :** Le code injecté interceptait les transactions de cryptomonnaies dans le navigateur, redirigeant les fonds vers les comptes des attaquants.
*   **Vulnérabilité de la Chaîne d'Approvisionnement :** L'attaque exploite la dépendance des développeurs envers des bibliothèques tierces.
*   **Risque Accru :** Une charge utile différente aurait pu avoir des conséquences beaucoup plus dévastatrices.

**Vulnérabilités :**

*   **Phishing et Authentification Faillible :** La méthode de 2FA utilisée (potentiellement basée sur des jetons interceptables) n'était pas suffisamment robuste contre le phishing. Bien que non spécifié avec un CVE, le mécanisme de 2FA compromis est la faille principale. L'article suggère que des clés de sécurité matérielles "phish-proof" auraient pu empêcher cet incident.

**Recommandations :**

*   **Authentification Résistante au Phishing :** Les plateformes comme NPM devraient exiger des méthodes d'authentification à deux facteurs résistantes au phishing, telles que les clés de sécurité matérielles, pour les comptes des contributeurs aux paquets critiques.
*   **Vérification Approfondie du Code :** Des mécanismes plus robustes de vérification et d'attestation de la provenance du code sont nécessaires avant d'accepter de nouvelles mises à jour pour des paquets largement utilisés.
*   **Surveillance et Détection :** Les outils de surveillance du code, comme ceux d'Aikido, sont essentiels pour identifier rapidement les modifications suspectes dans les dépôts de code.
*   **Renforcement des Pratiques de Sécurité :** Les développeurs doivent être vigilants face aux tentatives de phishing et adopter des mesures de sécurité strictes pour leurs comptes.

---
[Source](https://krebsonsecurity.com/2025/09/18-popular-code-packages-hacked-rigged-to-steal-crypto/){:target="_blank"}
