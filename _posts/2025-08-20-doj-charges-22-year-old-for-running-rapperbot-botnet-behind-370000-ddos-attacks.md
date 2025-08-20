---
title: 'DOJ Charges 22-Year-Old for Running RapperBot Botnet Behind 370,000 DDoS Attacks'
date: 2025-08-20
permalink: /posts/2025/08/20/doj-charges-22-year-old-for-running-rapperbot-botnet-behind-370000-ddos-attacks/
tags:
- veille-cyber
- hackernews
---
**Démantèlement du Botnet RapperBot**

Un individu de 22 ans, Ethan Foltz, originaire de l'Oregon, a été accusé par le Département de la Justice américain d'avoir créé et géré le botnet RapperBot. Ce service de location de attaques par déni de service distribué (DDoS) est opérationnel depuis au moins 2021 et a été utilisé pour mener plus de 370 000 attaques contre des victimes dans plus de 80 pays. Les attaques pouvaient atteindre des débits de plusieurs térabits par seconde (Tbps) et visaient à extorquer des victimes.

**Points Clés :**

*   **Administration :** Ethan Foltz est identifié comme l'administrateur du botnet RapperBot.
*   **Fonctionnement :** RapperBot infecte des appareils IoT, tels que des enregistreurs vidéo numériques (DVR) et des routeurs Wi-Fi, en utilisant des attaques par force brute sur SSH et Telnet. Les appareils compromis sont ensuite utilisés pour générer du trafic DDoS massif.
*   **Monétisation :** Le botnet a été monétisé en offrant des services d'attaque DDoS à des clients payants.
*   **Évolution :** En plus des attaques DDoS, RapperBot a été utilisé pour le cryptojacking (minage illicite de Monero) et a ciblé des services comme DeepSeek et X.
*   **Envergure :** Le botnet aurait compromis entre 65 000 et 95 000 appareils, menant des attaques atteignant jusqu'à 6 Tbps.
*   **Enquête :** Les autorités ont pu retracer le botnet jusqu'à Foltz grâce à des liens d'adresses IP avec des services en ligne qu'il utilisait et à ses recherches en ligne sur "RapperBot".
*   **Opération :** Le démantèlement de RapperBot fait partie de "Operation PowerOFF", une initiative internationale visant à démanteler les infrastructures de cybercriminalité DDoS.

**Vulnérabilités :**

*   **Brute-force SSH/Telnet :** Le botnet exploite la vulnérabilité des appareils IoT aux attaques par force brute sur les protocoles SSH et Telnet pour obtenir un accès non autorisé. Bien qu'aucun CVE spécifique ne soit mentionné dans l'article pour cette méthode, l'exploitation de ces protocoles sans mesures de sécurité adéquates est une faiblesse courante des appareils IoT.

**Recommandations :**

Bien que l'article ne contienne pas de recommandations directes adressées aux utilisateurs, les actions suivantes sont implicitement suggérées par la nature du botnet et l'enquête :

*   **Sécurisation des appareils IoT :** Les utilisateurs d'appareils IoT doivent s'assurer que leurs appareils sont protégés par des mots de passe forts et uniques, et que les protocoles comme SSH et Telnet ne sont pas accessibles depuis Internet sans authentification appropriée.
*   **Mises à jour logicielles :** Maintenir à jour le firmware des routeurs et autres appareils connectés est crucial pour corriger les vulnérabilités connues.
*   **Surveillance du trafic réseau :** Une surveillance accrue du trafic réseau peut aider à détecter des activités suspectes liées à des botnets.

---
[Source](https://thehackernews.com/2025/08/doj-charges-22-year-old-for-running.html){:target="_blank"}
