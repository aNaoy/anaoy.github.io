---
title: 'Mustang Panda Deploys SnakeDisk USB Worm to Deliver Yokai Backdoor on Thailand IPs'
date: 2025-09-15
permalink: /posts/2025/09/15/mustang-panda-deploys-snakedisk-usb-worm-to-deliver-yokai-backdoor-on-thailand-ips/
tags:
- veille-cyber
- hackernews
---
### Mustang Panda Élargit son Arsenal avec un Ver USB et une Nouvelle Variante de Backdoor

Le groupe de pirates informatiques lié à la Chine, Mustang Panda, déploie de nouveaux outils pour mener ses attaques. Il utilise une version mise à jour de la backdoor TONESHELL, désignée TONESHELL8 et TONESHELL9, ainsi qu'un ver USB inédit nommé SnakeDisk.

Le ver SnakeDisk est spécifiquement conçu pour ne s'exécuter que sur des systèmes situés en Thaïlande. Son objectif est de déposer la backdoor Yokai, qui permet d'établir une connexion inverse pour exécuter des commandes arbitraires. Yokai présente des similarités avec d'autres backdoors attribuées à ce groupe, comme PUBLOAD/PUBSHELL et TONESHELL, partageant des structures et des techniques similaires pour la communication avec les serveurs de commande et de contrôle (C2).

Les chercheurs ont également noté que TONESHELL8 et TONESHELL9 ont été modifiées pour communiquer via des serveurs proxy locaux, facilitant ainsi leur dissimulation dans le trafic réseau des entreprises. Ces nouvelles variantes intègrent également du code superflu récupéré sur le site de ChatGPT d'OpenAI afin de déjouer les analyses statiques.

SnakeDisk, qui partage des caractéristiques avec un autre ver USB nommé TONEDISK (également connu sous le nom de WispRider), se propage en détectant et en infectant les nouveaux périphériques USB connectés. Il masque les fichiers existants dans un nouveau sous-répertoire et remplace un fichier exécutable par un nom qui imite le nom du volume du disque ou "USB.exe" pour inciter l'utilisateur à l'ouvrir sur un nouveau système. Une fois le malware exécuté, les fichiers d'origine sont restaurés.

L'utilisation de SnakeDisk et Yokai suggère qu'un sous-groupe au sein de Mustang Panda se concentre particulièrement sur la Thaïlande, tout en démontrant la capacité d'évolution constante de cet acteur de menace.

**Points Clés:**

*   Mustang Panda utilise une backdoor TONESHELL mise à jour et un nouveau ver USB SnakeDisk.
*   SnakeDisk est géolocalisé pour cibler spécifiquement les adresses IP thaïlandaises.
*   SnakeDisk déploie la backdoor Yokai, qui permet l'exécution de commandes à distance.
*   Les nouvelles variantes de TONESHELL (TONESHELL8 et TONESHELL9) utilisent des proxys locaux pour la communication C2 et intègrent du code obsolète d'OpenAI pour éviter la détection.
*   SnakeDisk se propage via des clés USB en créant une fausse copie des fichiers légitimes pour masquer le malware.

**Vulnérabilités:**

*   L'article ne mentionne pas de CVEs spécifiques pour les vulnérabilités exploitées. Les méthodes d'infection semblent reposer sur l'ingénierie sociale (e-mails d'hameçonnage) et l'exploitation de la confiance envers les périphériques USB.

**Recommandations:**

*   Être vigilant face aux e-mails d'hameçonnage suspects.
*   Scanner systématiquement les périphériques USB avant de les utiliser sur un système.
*   Mettre à jour régulièrement les logiciels de sécurité et les systèmes d'exploitation.
*   Surveiller le trafic réseau pour détecter des activités suspectes, notamment des communications via des proxys locaux non autorisés.

---
[Source](https://thehackernews.com/2025/09/mustang-panda-deploys-snakedisk-usb.html){:target="_blank"}
