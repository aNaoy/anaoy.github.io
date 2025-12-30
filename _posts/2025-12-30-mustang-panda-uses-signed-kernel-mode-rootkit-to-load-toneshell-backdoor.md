---
title: 'Mustang Panda Uses Signed Kernel-Mode Rootkit to Load TONESHELL Backdoor'
date: 2025-12-30
permalink: /posts/2025/12/30/mustang-panda-uses-signed-kernel-mode-rootkit-to-load-toneshell-backdoor/
tags:
- veille-cyber
- hackernews
---
## Le rootkit TONESHELL de Mustang Panda

Le groupe de cyberespionnage chinois Mustang Panda a été observé utilisant un rootkit en mode noyau jusqu'alors inconnu pour déployer une nouvelle variante de sa backdoor TONESHELL. Cette attaque, ciblant des entités en Asie, notamment des organisations gouvernementales en Birmanie et en Thaïlande, met en évidence une évolution de leurs techniques visant à améliorer la furtivité et la résilience.

**Points clés:**

*   Mustang Panda utilise un rootkit en mode noyau signé avec un certificat numérique périmé ou volé pour masquer ses activités.
*   Le rootkit s'enregistre comme un pilote de filtre minime et injecte la backdoor TONESHELL dans les processus système.
*   TONESHELL est une backdoor capable d'établir un shell inversé et de télécharger des malwares supplémentaires.
*   Le groupe a également été lié à l'utilisation de TONEDISK, un ver USB, pour la distribution de sa backdoor Yokai.
*   L'infrastructure de commande et contrôle (C2) pour TONESHELL a été établie en septembre 2024, mais la campagne n'a débuté qu'en février 2025.
*   L'accès initial utilisé pour cette attaque n'est pas clair, mais il est suspecté que des machines compromises précédemment ont été utilisées.

**Vulnérabilités et Techniques d'Attaque:**

*   **Utilisation d'un rootkit en mode noyau:** Le rootkit, sous le nom de "ProjectConfiguration.sys", se dissimule dans le noyau du système d'exploitation, le rendant difficile à détecter par les solutions de sécurité traditionnelles.
*   **Signature numérique compromise:** Le pilote est signé avec un certificat numérique obsolète de Guangzhou Kingteller Technology Co., Ltd, suggérant l'exploitation d'un certificat divulgué ou volé.
*   **Manipulation des altitudes des pilotes:** Le rootkit interfère avec le pilote Microsoft Defender (WdFilter.sys) en modifiant son altitude d'exécution, lui permettant de contourner les contrôles de sécurité en se positionnant plus bas dans la pile d'E/S.
*   **Protection des processus et des clés de registre:** Le rootkit empêche la suppression ou la modification de ses propres fichiers et de ceux de TONESHELL en surveillant les opérations de suppression/renommage de fichiers et en bloquant les tentatives de création ou d'ouverture de clés de registre spécifiques.
*   **Injection de shellcode en mémoire:** Le rootkit dépose deux shellcodes en mode utilisateur qui sont exécutés dans des threads séparés. L'un injecte un petit shellcode créant un délai, tandis que l'autre injecte la backdoor TONESHELL dans un processus "svchost.exe".
*   **Communication C2 sur port 443:** TONESHELL communique avec ses serveurs C2 ("avocadomechanism[.]com" ou "potherbreference[.]com") en utilisant le port 443, un port couramment utilisé pour le trafic HTTPS, ce qui contribue à masquer sa communication.

**Recommandations:**

*   **Analyse forensique en mémoire:** La détection du shellcode injecté en mémoire est cruciale pour identifier la présence de TONESHELL sur les systèmes compromis.
*   **Surveillance des anomalies au niveau du noyau:** Les solutions de sécurité devraient se concentrer sur la détection d'activités suspectes au niveau du noyau, notamment les modifications de pilotes et les manipulations d'altitudes.
*   **Gestion stricte des certificats numériques:** Les organisations doivent s'assurer que les certificats numériques utilisés pour signer les logiciels sont valides et gérés de manière sécurisée pour éviter leur exploitation.
*   **Mises à jour et Patchs de sécurité:** Maintenir les systèmes d'exploitation et les logiciels de sécurité à jour est essentiel pour corriger les vulnérabilités qui pourraient être exploitées.
*   **Surveillance des communications C2:** Les équipes de sécurité devraient surveiller les communications réseau vers les adresses IP et domaines associés aux serveurs C2 connus de Mustang Panda.

---
[Source](https://thehackernews.com/2025/12/mustang-panda-uses-signed-kernel-driver.html){:target="_blank"}
