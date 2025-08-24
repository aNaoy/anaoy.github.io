---
title: 'Malicious Go Module Poses as SSH Brute-Force Tool, Steals Credentials via Telegram Bot'
date: 2025-08-24
permalink: /posts/2025/08/24/malicious-go-module-poses-as-ssh-brute-force-tool-steals-credentials-via-telegram-bot/
tags:
- veille-cyber
- hackernews
---
### Vol de d'identifiants via un module Go malveillant

Une nouvelle menace dans la chaîne d'approvisionnement logicielle a été identifiée : un module Go malveillant se faisant passer pour un outil de brute-force SSH. Son véritable objectif est d'exfiltrer discrètement les identifiants compromis vers un bot Telegram contrôlé par le cybercriminel.

Ce package, nommé "golang-random-ip-ssh-bruteforce", a été publié sur pkg.go.dev en juin 2022 et est associé à un compte GitHub désormais inaccessible. Il scanne aléatoirement des adresses IP pour trouver des services SSH ouverts sur le port 22. Ensuite, il tente de se connecter en utilisant une liste intégrée de noms d'utilisateur (root, admin) et de mots de passe faibles (password, 12345678, qwerty, etc.).

Une caractéristique notable de ce malware est qu'il désactive la vérification des clés hôtes SSH en utilisant `ssh.InsecureIgnoreHostKey`. Cela permet au client SSH d'accepter des connexions de n'importe quel serveur, indépendamment de son identité. Une fois qu'un identifiant valide est trouvé, l'adresse IP de la cible, le nom d'utilisateur et le mot de passe sont envoyés via l'API Telegram à un bot spécifique, "@sshZXC_bot", appartenant à l'attaquant identifié sous le pseudonyme "@io_ping".

Le module a été conçu pour fonctionner en boucle infinie, en générant des adresses IP et en tentant des connexions SSH simultanées avec la liste prédéfinie. Le trafic envoyé via l'API Telegram utilise HTTPS, ce qui lui permet de se fondre dans le trafic web légitime et potentiellement d'éviter les contrôles de sortie.

L'attaquant, présumé d'origine russe, a également développé d'autres outils, notamment un scanner de ports IP, un analyseur de profils et de médias Instagram, et un botnet PHP de commande et contrôle nommé Selica-C2. Son activité passée inclut des vidéos sur la manière de pirater des bots Telegram et la création d'un "SMS bomber" puissant.

**Points clés :**

*   Un module Go se fait passer pour un outil de brute-force SSH.
*   Il exfiltre les identifiants réussis vers un bot Telegram.
*   Il désactive la vérification des clés hôtes SSH.
*   Il cible des services SSH ouverts sur le port 22.
*   L'attaquant est présumé d'origine russe.

**Vulnérabilités :**

*   Aucune vulnérabilité CVE spécifique n'est mentionnée dans l'article. La menace réside dans l'utilisation d'un module malveillant qui **exploite les pratiques de configuration SSH peu sécurisées (comme la désactivation de la vérification des clés hôtes)** et la **prolifération de mots de passe faibles**.

**Recommandations :**

*   Utiliser des **politiques de sécurité robustes pour la chaîne d'approvisionnement logicielle**, incluant l'analyse des dépendances et des modules utilisés.
*   **Éviter l'utilisation de fonctions telles que `ssh.InsecureIgnoreHostKey`** qui désactivent la vérification des clés hôtes.
*   **Appliquer des mots de passe forts et uniques** et ne pas utiliser ceux présents dans la liste du malware.
*   **Mettre en place des contrôles de sécurité réseau stricts** pour surveiller et filtrer le trafic sortant suspect, même s'il utilise HTTPS.
*   **Restreindre l'accès aux services SSH** uniquement aux adresses IP autorisées.

---
[Source](https://thehackernews.com/2025/08/malicious-go-module-poses-as-ssh-brute.html){:target="_blank"}
