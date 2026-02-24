---
title: 'MuddyWater Targets MENA Organizations with GhostFetch, CHAR, and HTTP_VIP'
date: 2026-02-24
permalink: /posts/2026/02/24/muddywater-targets-mena-organizations-with-ghostfetch-char-and-http-vip/
tags:
- veille-cyber
- hackernews
---
**MuddyWater intensifie ses attaques dans la région MENA avec de nouveaux outils**

Un groupe de cyberespionnage iranien, connu sous le nom de MuddyWater, a lancé une nouvelle campagne d'attaques baptisée "Opération Olalampo" visant des organisations et des individus principalement situés au Moyen-Orient et en Afrique du Nord (MENA).

L'approche typique de MuddyWater consiste à envoyer des e-mails de phishing contenant des documents Microsoft Office malveillants. L'ouverture de ces documents et l'activation des macros déclenchent l'exécution de code, permettant au groupe de prendre le contrôle à distance des systèmes compromis.

Plusieurs nouvelles familles de logiciels malveillants ont été déployées, partageant des caractéristiques avec des outils précédemment utilisés par le groupe :

*   **GhostFetch :** Un téléchargeur de premier étage qui effectue un profilage du système, vérifie la présence de dispositifs de débogage, de machines virtuelles et de logiciels antivirus, avant de télécharger et d'exécuter des charges utiles secondaires en mémoire.
*   **GhostBackDoor :** Un malware de second étage, déployé par GhostFetch, qui offre un shell interactif, la possibilité de lire/écrire des fichiers et de relancer GhostFetch.
*   **HTTP_VIP :** Un téléchargeur natif qui effectue une reconnaissance du système et se connecte à un serveur externe pour déployer le logiciel de bureau à distance AnyDesk. Des variantes plus récentes peuvent également collecter des informations sur la victime et exécuter des commandes interactives.
*   **CHAR :** Un malware écrit en Rust, contrôlé via un bot Telegram, capable de changer de répertoire et d'exécuter des commandes système. L'analyse de son code source suggère l'utilisation d'outils de développement assistés par IA.

MuddyWater exploite également des vulnérabilités récemment divulguées sur des serveurs publics pour obtenir un accès initial aux réseaux cibles. L'adoption continue de technologies d'IA, le développement de logiciels malveillants personnalisés et la diversification de ses infrastructures de commande et contrôle soulignent l'intention du groupe d'étendre ses opérations dans la région.

**Points clés :**

*   Groupe : MuddyWater (alias Earth Vetala, Mango Sandstorm, MUDDYCOAST)
*   Région ciblée : Moyen-Orient et Afrique du Nord (MENA)
*   Nom de l'opération : Opération Olalampo
*   Méthode d'infection principale : E-mails de phishing avec documents Office malveillants, activation de macros.
*   Nouveaux outils malveillants : GhostFetch, GhostBackDoor, HTTP_VIP, CHAR.
*   Utilisation potentielle de l'IA dans le développement de malware.
*   Exploitation de vulnérabilités publiques.

**Vulnérabilités :**

*   Non spécifiées par leur identifiant CVE, mais l'article mentionne l'exploitation de "vulnérabilités récemment divulguées sur des serveurs publics".

**Recommandations :**

*   Les organisations doivent rester vigilantes face aux e-mails de phishing et à la demande d'activation de macros dans les documents reçus.
*   Maintenir les systèmes et les logiciels à jour pour corriger les vulnérabilités connues.
*   Implémenter des mesures de sécurité robustes, y compris des solutions antivirus et de détection d'intrusion.
*   Sensibiliser les utilisateurs aux risques de cybersécurité.

---
[Source](https://thehackernews.com/2026/02/muddywater-targets-mena-organizations.html){:target="_blank"}
