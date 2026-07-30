---
title: 'Amazon links Debug, Chalk NPM supply-chain attacks to North Korean hackers'
date: 2026-07-30
permalink: /posts/2026/07/30/amazon-links-debug-chalk-npm-supply-chain-attacks-to-north-korean-hackers/
tags:
- veille-cyber
- bleepingcomp
---
### Attaques sur la chaîne d'approvisionnement NPM par le groupe nord-coréen Sapphire Sleet

Amazon a formellement lié une série d'attaques sophistiquées sur la chaîne d'approvisionnement logicielle (écosystème NPM) au groupe de hackers nord-coréen **Sapphire Sleet** (également connu sous les noms BlueNoroff ou Stardust Chollima). Ces attaques visent à compromettre des bibliothèques logicielles largement utilisées pour obtenir un accès indirect à de vastes infrastructures cloud.

**Points clés**
*   **Cibles majeures :** Les bibliothèques populaires `typo-crypto`, `debug`, `chalk` et `axios` ont été compromises par des mises à jour malveillantes.
*   **Méthodologie :** Les attaquants utilisent l'ingénierie sociale pour compromettre les comptes des mainteneurs de paquets, publiant ensuite du code malveillant diffusé automatiquement aux utilisateurs.
*   **Évolution des menaces :** Les attaquants gagnent la confiance de la communauté sur plusieurs mois, utilisent des tactiques de « slopsquatting » (exploitation de noms de paquets suggérés par des IA) et découpent les fonctionnalités malveillantes en plusieurs petits paquets pour échapper à la détection.
*   **Motivation :** Essentiellement financière, cherchant à maximiser le nombre de victimes en aval via des composants largement intégrés.

**Vulnérabilités observées**
*   **Ingénierie sociale :** Compromission des identifiants des mainteneurs.
*   **Évasion par IA :** Exploitation des hallucinations d'assistants de codage générant des dépendances inexistantes (slopsquatting).
*   **Obfuscation avancée :** Utilisation de charges utiles multi-étapes, de serveurs de commande et contrôle (C2) dynamiques et de payloads sensibles à l'environnement (détection des bacs à sable).

**Recommandations**
*   **Vigilance sur les dépendances :** Auditer systématiquement les mises à jour des bibliothèques tierces, surtout pour les paquets très populaires.
*   **Analyse statique et dynamique :** Ne pas se fier uniquement à l'analyse statique ; utiliser des outils de simulation de brèche pour tester la robustesse des règles de détection (EDR/SIEM).
*   **Protection des comptes :** Renforcer la sécurité des comptes des mainteneurs (authentification multifactorielle stricte, gestion rigoureuse des accès).
*   **Collaboration communautaire :** S'appuyer sur les initiatives de sécurité Open Source (type OpenSSF ou Akrites) pour identifier les paquets suspects et partager les renseignements sur les menaces.

---
[Source](https://www.bleepingcomputer.com/news/security/amazon-links-debug-chalk-npm-supply-chain-attacks-to-north-korean-hackers/){:target="_blank"}
