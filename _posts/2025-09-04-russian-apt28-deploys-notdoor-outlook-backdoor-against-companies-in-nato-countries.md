---
title: 'Russian APT28 Deploys “NotDoor” Outlook Backdoor Against Companies in NATO Countries'
date: 2025-09-04
permalink: /posts/2025/09/04/russian-apt28-deploys-notdoor-outlook-backdoor-against-companies-in-nato-countries/
tags:
- veille-cyber
- hackernews
---
## APT28 déploie la porte dérobée NotDoor sur Outlook

Le groupe de pirates informatiques parrainé par l'État russe, APT28, utilise une nouvelle porte dérobée pour Microsoft Outlook baptisée "NotDoor" dans des attaques visant des entreprises situées dans des pays membres de l'OTAN.

NotDoor est un script VBA conçu pour Outlook, capable de surveiller les e-mails entrants à la recherche d'un mot déclencheur spécifique. Une fois détecté, il permet aux attaquants d'exfiltrer des données, de télécharger des fichiers et d'exécuter des commandes sur l'ordinateur de la victime. Le nom "NotDoor" provient de l'utilisation du mot "Nothing" dans son code source.

L'accès initial exact pour déployer le malware n'est pas encore connu, mais les analyses indiquent qu'il est distribué via l'exécutable OneDrive ("onedrive.exe") grâce à une technique de "DLL side-loading". Cela mène à l'exécution d'une DLL malveillante ("SSPICLI.dll") qui installe la porte dérobée VBA et désactive les protections de sécurité des macros pour échapper à la détection.

NotDoor utilise les événements `Application.MAPILogonComplete` et `Application.NewMailEx` d'Outlook pour s'exécuter à chaque démarrage d'Outlook ou à la réception d'un nouvel e-mail. Il crée un dossier temporaire pour stocker les fichiers à exfiltrer via une adresse Proton Mail. Il analyse les e-mails entrants pour trouver une chaîne de déclenchement, telle que "Daily Report", pour exécuter des commandes intégrées.

Le malware prend en charge quatre commandes :
*   `cmd` : Exécute des commandes et renvoie la sortie standard sous forme de pièce jointe d'e-mail.
*   `cmdno` : Exécute des commandes.
*   `dwn` : Exfiltre des fichiers de l'ordinateur de la victime en les envoyant comme pièces jointes d'e-mail.
*   `upl` : Dépose des fichiers sur l'ordinateur de la victime.

Les fichiers exfiltrés sont chiffrés avec le chiffrement personnalisé du malware, envoyés par e-mail, puis supprimés du système.

Ces attaques sont également notables pour l'utilisation abusive des Microsoft Dev Tunnels (devtunnels.ms) comme domaines de commande et de contrôle (C2) pour plus de discrétion. Cette technique masque l'adresse IP du serveur C2 et permet aux attaquants de faire pivoter rapidement leur infrastructure en exploitant la confiance et le volume de trafic des services cloud grand public.

**Points clés :**
*   **Groupe de menace :** APT28 (parrainé par l'État russe)
*   **Malware :** NotDoor (porte dérobée VBA pour Microsoft Outlook)
*   **Cible :** Entreprises dans des pays membres de l'OTAN
*   **Fonctionnalités :** Surveillance des e-mails, exfiltration de données, exécution de commandes, téléchargement/envoi de fichiers.
*   **Mécanisme d'infection :** DLL side-loading via `onedrive.exe`, désactivation des protections de macros.
*   **Canal de communication C2 :** Utilisation abusive de Microsoft Dev Tunnels pour masquer l'infrastructure.

**Vulnérabilités potentielles :**
Aucune CVE spécifique n'est mentionnée dans l'article concernant NotDoor lui-même. Cependant, l'article souligne l'exploitation de fonctionnalités légitimes (macros Outlook, OneDrive, Dev Tunnels) qui, lorsqu'elles sont détournées, peuvent conduire à une compromission. L'efficacité du malware repose également sur le fait que les utilisateurs ne prêtent pas attention aux messages de sécurité des macros ou ouvrent des pièces jointes provenant d'e-mails suspects.

**Recommandations :**
*   Maintenir Microsoft Outlook et les autres applications Microsoft à jour.
*   Sensibiliser les utilisateurs aux risques liés aux macros et les inciter à ne pas les activer pour des documents provenant de sources non fiables.
*   Revoir et renforcer les politiques de sécurité relatives à l'exécution des macros.
*   Surveiller le trafic réseau sortant pour détecter toute communication suspecte vers des adresses inconnues ou des services cloud inhabituels.
*   Examiner les logs d'événements pour détecter des activités suspectes liées à `onedrive.exe` et à l'exécution de scripts PowerShell.
*   Envisager des solutions de sécurité avancées pour la détection des menaces basées sur le comportement et l'analyse de l'apprentissage automatique.

---
[Source](https://thehackernews.com/2025/09/russian-apt28-deploys-notdoor-outlook.html){:target="_blank"}
