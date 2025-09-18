---
title: 'Exploring Uploads in a Dshield Honeypot Environment &#x5b;Guest Diary&#x5d;, (Thu, Sep 18th)'
date: 2025-09-18
permalink: /posts/2025/09/18/exploring-uploads-in-a-dshield-honeypot-environment-x5bguest-diaryx5d-thu-sep-18th/
tags:
- veille-cyber
- sans-isc
---
### Analyse des Fichiers Téléversés : Une Plongée dans les Menaces

Une analyse des fichiers téléversés vers un serveur honeypot Cowrie a révélé deux types d'activités malveillantes distinctes. L'outil `upload-stats` a permis d'identifier des scripts de téléchargement de charges utiles malveillantes et des composants de ver botnet ciblant des appareils IoT et des systèmes potentiellement obsolètes.

**Points Clés :**

*   **Scripts de Téléchargement de Charges Utiles :** Un script identifié vise à télécharger des charges utiles spécifiques à diverses architectures de processeurs via FTP. Le script tente de se déplacer dans plusieurs répertoires avant de télécharger le fichier, lui donne les permissions d'exécution, et l'exécute en lui passant potentiellement le paramètre "telnet". Il supprime ensuite le fichier téléchargé pour masquer ses traces. L'adresse IP du serveur FTP (87.121.84.163) est associée à un fournisseur néerlandais de VPS opérant au Royaume-Uni, bien que certains rapports la localisent en Bulgarie.
*   **Ver Botnet UNIX_PIMINE.A :** Des fichiers classés comme "data" ont révélé des éléments d'un ver botnet, identifié comme UNIX_PIMINE.A. Ces fichiers provenaient de sessions SSH actives où des commandes étaient exécutées via stdin. Le malware semble cibler des appareils IoT, notamment des Raspberry Pi, en utilisant des paires d'identifiants "pi/raspberry" et une combinaison plus spécifique "pi/raspberryraspberry993311", potentiellement liée à d'autres souches malveillantes. Il modifie le système pour s'exécuter au redémarrage, supprime d'autres logiciels malveillants (probablement des mineurs de cryptomonnaies) et communique via un canal IRC (#biret). Pour se propager, il utilise `sshpass` et `Zmap` pour scanner le port 22 et tenter des connexions SSH avec les identifiants mentionnés. Les adresses sources identifiées (81.172.146.181 et 176.188.22.163) correspondent à des victimes compromises, respectivement d'un fournisseur d'accès néerlandais et français.

**Vulnérabilités identifiées (non spécifiées avec CVE dans l'article) :**

*   Utilisation de protocoles non sécurisés comme le FTP en clair pour la distribution de charges utiles.
*   Ciblage d'appareils IoT et de systèmes potentiellement mal configurés ou obsolètes.
*   Exploitation de mots de passe par défaut ou faibles ("raspberry").
*   Mécanismes de propagation par SSH exploitant les identifiants par défaut.

**Recommandations :**

*   Maintenir les systèmes à jour et surveiller activement les environnements informatiques.
*   Changer impérativement les mots de passe par défaut sur tous les appareils connectés à Internet, en particulier les appareils IoT.
*   Utiliser des outils d'analyse et d'automatisation pour corréler les journaux d'événements avec les fichiers téléversés afin de mieux comprendre les schémas d'attaque.

---
[Source](https://isc.sans.edu/diary/rss/32296){:target="_blank"}
