---
title: 'Transparent Tribe Launches New RAT Attacks Against Indian Government and Academia'
date: 2026-01-02
permalink: /posts/2026/01/02/transparent-tribe-launches-new-rat-attacks-against-indian-government-and-academia/
tags:
- veille-cyber
- hackernews
---
## Cyberattaques Ciblées en Inde : Nouvelles Tactiques de Transparent Tribe et Patchwork

Des groupes de cyberespionnage, notamment Transparent Tribe (APT36) et Patchwork, intensifient leurs attaques contre des entités gouvernementales, universitaires et stratégiques en Inde. Ces acteurs exploitent des techniques sophistiquées pour déployer des chevaux de Troie d'accès à distance (RAT) et obtenir un contrôle persistant sur les systèmes compromis.

**Points Clés et Vulnérabilités :**

*   **Transparent Tribe (APT36)** :
    *   **Méthode d'attaque initiale** : Campagnes d'hameçonnage ciblées utilisant des fichiers raccourcis Windows (LNK) déguisés en documents PDF. Ces fichiers déclenchent l'exécution de scripts HTML (HTA) qui décryptent et chargent la charge utile RAT directement en mémoire, tout en affichant un document PDF leurre pour masquer l'activité.
    *   **Ingénierie sociale** : Utilisation de courriels d'hameçonnage contenant des archives ZIP avec des fichiers LNK trompeurs.
    *   **Exploitation de "mshta.exe"** : Utilisation de l'application HTML (HTA) et de l'objet ActiveX "WScript.Shell" pour interagir avec l'environnement Windows, effectuer un profilage du système et manipuler l'exécution pour une fiabilité accrue.
    *   **Adaptation de la persistance** : Mécanismes de persistance variés en fonction de la solution antivirus détectée sur la machine infectée :
        *   Kaspersky : Création d'un répertoire de travail, obfuscation de la charge utile HTA, et établissement de la persistance via un fichier LNK dans le dossier de démarrage.
        *   Quick Heal : Création d'un fichier batch et d'un fichier LNK malveillant dans le dossier de démarrage, appelés par le script batch.
        *   Avast, AVG, Avira : Copie directe de la charge utile dans le répertoire de démarrage pour exécution.
        *   Absence d'antivirus détecté : Combinaison de fichiers batch, de persistance via le registre et de déploiement de la charge utile.
    *   **RAT fonctionnel** : La charge utile finale (par exemple, "iinneldc.dll" ou "wininet.dll") est un RAT complet capable de contrôler le système à distance, de gérer des fichiers, d'exfiltrer des données, de capturer des captures d'écran, de manipuler le presse-papiers et de contrôler des processus.
    *   **Commandes C2** : Utilisation de points de terminaison HTTP GET pour communiquer avec l'infrastructure de commande et de contrôle (C2), tels que `/retsiger` (enregistrer), `/taebtraeh` (batement de cœur), `/dnammoc_teg` (obtenir commande), et `/dnammocmvitna` (commande antivm). Les caractères des points de terminaison sont inversés pour échapper à la détection statique.
    *   **Autre campagne** : Utilisation d'un fichier raccourci déguisé en avis du gouvernement ("NCERT-Whatsapp-Advisory.pdf.lnk") pour livrer un chargeur basé sur .NET, qui déploie ensuite des exécutables supplémentaires et des DLL malveillantes. Ce processus implique la récupération d'un installateur MSI ("nikmights.msi") à partir d'un serveur distant pour exécuter une série d'actions, y compris le déploiement de DLL ("pdf.dll", "wininet.dll") et d'un exécutable ("PcDirvs.exe") avec persistance via le registre et un fichier HTA.

*   **Patchwork** :
    *   **Ciblage du secteur de la défense pakistanaise** : Utilisation d'un chargeur basé sur MSBuild déguisé dans des fichiers ZIP, déployant une RAT Python.
    *   **Capacités de la RAT Python** : Communication avec le C2, exécution de modules Python à distance, exécution de commandes, et transfert de fichiers.
    *   **Outils modernes et obfusqués** : Utilisation de chargeurs LOLBin MSBuild, de runtimes Python modifiés par PyInstaller, d'implants en bytecode marshalisé, de géolocalisation, de points de terminaison PHP C2 aléatoires et de mécanismes de persistance réalistes.
    *   **Nouveau Trojan StreamSpy** : Utilisation des protocoles WebSocket pour recevoir des instructions et transmettre les résultats d'exécution, et HTTP pour les transferts de fichiers. Ce trojan présente des similitudes avec "Spyder", une variante du backdoor "WarHawk" attribué à SideWinder, et des échantillons corrélés suggèrent une possible mise en commun de ressources entre Maha Grass (Patchwork) et le groupe DoNot.
    *   **Distribution via des archives ZIP** : Utilisation d'archives ZIP ("OPS-VII-SIR.zip") hébergées sur des plateformes comme "firebasescloudemail[.]com" pour distribuer des exécutables malveillants comme "Annexure.exe".
    *   **Commandes StreamSpy** : Une large gamme de commandes supportées, notamment le téléchargement/ouverture de fichiers, la définition de shells pour l'exécution de commandes (cmd, PowerShell), le téléchargement et l'extraction de fichiers zip chiffrés, la collecte d'informations sur le système de fichiers, le téléchargement/téléchargement de fichiers, la suppression, le renommage et l'énumération de dossiers.
    *   **Lien avec ShadowAgent** : La signature numérique de "Annexure.exe" présente des corrélations avec "ShadowAgent", une autre RAT Windows attribuée au groupe DoNot, renforçant l'idée d'une possible collaboration ou d'un partage de ressources entre ces groupes.

**Recommandations :**

Bien que l'article ne détaille pas de recommandations spécifiques, les pratiques de cybersécurité générales s'appliquent :

*   **Vigilance accrue face aux courriels suspects** : Ne pas ouvrir de pièces jointes ou cliquer sur des liens provenant de sources inconnues ou non sollicitées.
*   **Mise à jour des systèmes et logiciels** : Assurer que tous les systèmes d'exploitation, navigateurs et applications sont à jour avec les derniers correctifs de sécurité.
*   **Utilisation de solutions de sécurité robustes** : Déployer et maintenir des logiciels antivirus et anti-malware à jour, ainsi que des pare-feux.
*   **Formation des utilisateurs** : Sensibiliser les utilisateurs aux techniques d'ingénierie sociale et aux menaces de phishing.
*   **Politiques de sécurité strictes** : Mettre en place des politiques de sécurité claires concernant l'utilisation des périphériques, le téléchargement de logiciels et l'accès aux informations sensibles.
*   **Surveillance du réseau et des journaux** : Mettre en œuvre une surveillance continue du réseau pour détecter les activités suspectes et analyser les journaux système pour identifier d'éventuelles compromissions.

---
[Source](https://thehackernews.com/2026/01/transparent-tribe-launches-new-rat.html){:target="_blank"}
