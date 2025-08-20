---
title: 'Oregon Man Charged in ‘Rapper Bot’ DDoS Service'
date: 2025-08-20
permalink: /posts/2025/08/20/oregon-man-charged-in-rapper-bot-ddos-service/
tags:
- veille-cyber
- krebs
---
## Rapper Bot : La chute d'un opérateur de botnet DDoS

Un individu de 22 ans de l'Oregon, Ethan J. Foltz, a été arrêté pour avoir exploité "Rapper Bot", un vaste réseau de dizaines de milliers d'appareils IoT compromis utilisé pour lancer des attaques par déni de service distribué (DDoS). Le botnet, qui pouvait générer des flux de données de plusieurs téraoctets par seconde, était loué à des groupes menant des activités d'extorsion, notamment contre des opérations de jeux d'argent en ligne basées en Chine. Il aurait été responsable d'une attaque ayant perturbé Twitter/X en mars 2025. Foltz opérait ce réseau avec un complice connu sous le pseudonyme "Slaykings".

### Points Clés

*   **Opération Rapper Bot :** Ethan J. Foltz est accusé d'avoir géré un botnet massif composé d'environ 65 000 appareils IoT.
*   **Service de location :** Le botnet était proposé à la location pour mener des attaques DDoS, principalement pour des opérations d'extorsion.
*   **Attaques puissantes :** Les attaques pouvaient dépasser les six téraoctets par seconde, visant à submerger les infrastructures cibles.
*   **Stratégie d'évitement :** Foltz et son complice ont cherché à rester discrets, notamment en évitant de cibler des journalistes spécialisés en cybersécurité comme Brian Krebs. Ils maintenaient le botnet à une taille "juste ce qu'il faut" pour être puissant mais difficilement détectable.
*   **Origine du code :** Rapper Bot utilise une grande partie de son code de la souche malveillante fBot (également connue sous le nom de Satori), elle-même dérivée du botnet Mirai.
*   **Enquêtes :** L'identification de Foltz a été facilitée par des procédures judiciaires impliquant son fournisseur d'accès à Internet, PayPal et Google, révélant ses recherches sur la cybersécurité et ses conversations sur Telegram avec Slaykings.
*   **Impact financier :** Les attaques pouvaient coûter entre 500 et 10 000 dollars aux victimes, les exposant souvent à des demandes d'extorsion.
*   **Moins de 60 secondes :** La durée typique des attaques pour la plupart des clients était limitée à 60 secondes pour minimiser l'attention.

### Vulnérabilités

Bien que l'article ne mentionne pas de CVE spécifiques pour les vulnérabilités exploitées par Rapper Bot, il est indiqué que le botnet utilise un code basé sur **fBot (Satori)**, qui est lui-même une variation du **Mirai IoT botnet**. Ces botnets sont connus pour exploiter des faiblesses dans les appareils IoT pour leur prise de contrôle. Foltz a également mentionné la découverte d'une nouvelle vulnérabilité permettant de compromettre 32 000 nouveaux appareils.

### Recommandations

L'article ne contient pas de recommandations directes dans le sens de conseils pratiques pour les utilisateurs finaux. Il met plutôt en évidence les actions des forces de l'ordre et les conséquences de ces activités cybercriminelles. Les implications suggérées pour la protection incluent :

*   **Sécurisation des appareils IoT :** Bien que non explicitement mentionné, la nature de ces botnets souligne l'importance de sécuriser correctement les appareils connectés pour prévenir leur compromission.
*   **Solutions de défense DDoS :** L'article mentionne l'existence et le coût des solutions de mitigation DDoS, suggérant que les entreprises doivent envisager de telles protections.
*   **Conscience des risques :** L'affaire démontre les risques financiers et opérationnels que représentent les attaques DDoS à grande échelle pour les entreprises.

---
[Source](https://krebsonsecurity.com/2025/08/oregon-man-charged-in-rapper-bot-ddos-service/){:target="_blank"}
