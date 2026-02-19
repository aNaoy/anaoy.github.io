---
title: 'Arkanix Stealer: a C++ & Python infostealer'
date: 2026-02-19
permalink: /posts/2026/02/19/arkanix-stealer-a-c-python-infostealer/
tags:
- veille-cyber
- securelist
---
**Arkanix Stealer : Une menace sophistiquée en version C++ et Python**

Un nouveau logiciel malveillant, baptisé "Arkanix Stealer", a été identifié en octobre 2025. Opérant selon un modèle de "malware-as-a-service" (MaaS), il propose aux utilisateurs non seulement l'implant, mais aussi un panneau de contrôle pour gérer les charges utiles et consulter les statistiques. Les auteurs auraient potentiellement utilisé des outils d'IA pour le développement.

**Points clés :**

*   **Modèle MaaS :** Offre un implant et un panneau de contrôle aux clients.
*   **Double implémentation :** Existe en versions C++ (native) et Python.
*   **Distribution :** Le vecteur d'infection initial est probablement le phishing, basé sur les noms de fichiers des scripts de chargement observés.
*   **Campagne de courte durée :** Le programme d'affiliation semble avoir été rapidement démantelé.
*   **Ciblage :** S'attaque aux données sensibles des utilisateurs, y compris les cryptomonnaies, les jeux et les informations bancaires.

**Vulnérabilités et Capacités :**

Arkanix Stealer collecte une vaste gamme d'informations :

*   **Informations système :** Version de l'OS, détails CPU/GPU, taille de la RAM, résolution d'écran, disposition du clavier, fuseau horaire, logiciels installés, antivirus, VPN.
*   **Données de navigation :** Historique, auto-remplissage (e-mails, numéros de téléphone, adresses, cartes de paiement), mots de passe enregistrés, cookies pour 22 navigateurs différents.
*   **Données Telegram :** Collecte du répertoire `tdata` (complet ou partiel selon la configuration).
*   **Informations Discord :** Vol d'identifiants et auto-propagation via l'API Discord.
*   **Identifiants VPN :** Cible des logiciels VPN populaires comme Mullvad, NordVPN, ExpressVPN, ProtonVPN.
*   **Fichiers divers :** Recherche et exfiltration de documents et de médias à partir de chemins prédéfinis et d'une liste de noms de fichiers spécifiques.
*   **Informations RDP :** Collecte des détails des connexions RDP connues (adresse serveur, mot de passe, nom d'utilisateur, port).
*   **Données de jeux :** Vol d'identifiants pour des plateformes comme Steam, Epic Games Launcher, Riot, Origin, etc.
*   **Captures d'écran :** La version native peut capturer des captures d'écran.
*   **Modules additionnels :** Télécharge potentiellement des modules tels qu'un "Chrome grabber", un "Wallet patcher" (ciblant Exodus et Atomic wallets), un "Extra collector" (incluant FileZilla, Steam, captures d'écran) et un composant HVNC (High-performance Virtual Network Computing).

**Vulnérabilités spécifiques exploitées (non directement liées à CVE pour le stealer lui-même, mais à ses capacités) :**

*   Les capacités de vol de mots de passe de navigateur et d'informations d'authentification sont rendues possibles par l'accès aux fichiers de stockage sécurisés des navigateurs et des applications, souvent protégés par des mécanismes comme DPAPI sur Windows.
*   Le vol d'informations Telegram exploite la manière dont l'application stocke ses données de session.
*   La fonction d'auto-propagation Discord tire parti des fonctionnalités de l'API Discord pour envoyer des messages à des contacts.
*   La version C++ intègre l'outil "ChromElevator", qui exploite des mécanismes d'injection de code et de syscalls pour accéder aux données des navigateurs.

**Recommandations :**

Bien que l'article ne contienne pas de section dédiée aux recommandations, les pratiques de sécurité standard s'appliquent :

*   **Prudence face au phishing :** Ne pas cliquer sur des liens suspects ou télécharger des pièces jointes provenant de sources non fiables.
*   **Mises à jour régulières :** Maintenir le système d'exploitation, les navigateurs et les logiciels de sécurité à jour pour corriger les vulnérabilités connues.
*   **Utilisation d'un antivirus/antimalware fiable :** S'assurer que le logiciel de sécurité est activé et mis à jour.
*   **Authentification multifacteur (MFA) :** Activer la MFA partout où c'est possible, en particulier pour les comptes sensibles (e-mail, réseaux sociaux, plateformes de cryptomonnaies).
*   **Sauvegardes régulières :** Effectuer des sauvegardes régulières des données importantes pour pouvoir les récupérer en cas d'incident.
*   **Surveillance du trafic réseau :** Les entreprises peuvent envisager de surveiller le trafic réseau à la recherche de communications suspectes vers les domaines identifiés (arkanix[.]pw, arkanix[.]ru).

---
[Source](https://securelist.com/arkanix-stealer/119006/){:target="_blank"}
