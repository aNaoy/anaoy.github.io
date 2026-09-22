---
title: 'SideCopy Broadens India Targeting to Academia With ReverseRAT Spear-Phishing'
date: 2026-09-22
permalink: /posts/2026/09/22/sidecopy-broadens-india-targeting-to-academia-with-reverserat-spear-phishing/
tags:
- veille-cyber
- hackernews
---
### Expansion des cyberattaques de SideCopy vers le secteur académique indien

Le groupe APT (Advanced Persistent Threat) **SideCopy**, actif depuis 2019 et lié au Pakistan, a étendu ses opérations de cyberespionnage aux institutions académiques indiennes, en complément de ses cibles habituelles (gouvernements et forces de défense).

**Points clés :**
*   **Vecteur d'attaque :** Campagnes de spear-phishing diffusant des archives ZIP contenant des raccourcis Windows (.LNK) malveillants masqués par des icônes de PDF.
*   **Mécanisme d'infection :** Utilisation abusive de `mshta.exe` pour exécuter des scripts HTA obfusqués, permettant un chargement réflexif de charges utiles directement en mémoire.
*   **Charge utile :** Déploiement de **ReverseRAT**, un cheval de Troie d'accès à distance capable de voler des données, d'exécuter des commandes, de capturer des écrans et de maintenir une persistance via le Registre Windows.
*   **Techniques d'évasion :** Utilisation de routines d'auto-suppression (anti-forensique), décodage en mémoire volatile et désérialisation .NET pour contourner les solutions de sécurité basées sur le disque.

**Vulnérabilités exploitées :**
*   Abus légitime de **mshta.exe** (Living-off-the-land) : Bien qu'il ne s'agisse pas d'une CVE spécifique, cette technique détourne un composant Windows standard pour exécuter des scripts malveillants.
*   **Désérialisation .NET non sécurisée :** Exploitée pour charger la charge utile ReverseRAT en mémoire.

**Recommandations :**
*   **Filtrage des courriels :** Renforcer les passerelles de messagerie pour détecter les pièces jointes suspectes (fichiers LNK, ZIP, HTA).
*   **Contrôle des applications :** Restreindre ou surveiller l'exécution de `mshta.exe` dans l'environnement, particulièrement lorsqu'il est appelé depuis des dossiers temporaires ou des fichiers provenant de l'extérieur.
*   **Surveillance réseau :** Bloquer les connexions sortantes vers les domaines suspects (`dns.educationportals[.]biz`) et surveiller les flux de données inhabituels sur le port 5863.
*   **Durcissement du système :** Désactiver les fonctionnalités de scripts non nécessaires et limiter les privilèges des utilisateurs pour prévenir l'installation de clés de persistance dans le Registre.

---
[Source](https://thehackernews.com/2026/09/sidecopy-broadens-india-targeting-to.html){:target="_blank"}
