---
title: 'Cloudflare blocks largest recorded DDoS attack peaking at 11.5 Tbps'
date: 2025-09-02
permalink: /posts/2025/09/02/cloudflare-blocks-largest-recorded-ddos-attack-peaking-at-115-tbps/
tags:
- veille-cyber
- bleepingcomp
---
**Cloudflare Dévie une Cyber-attaque d'une Ampleur Inédite**

L'entreprise d'infrastructure Internet Cloudflare a récemment déjoué la plus importante attaque par déni de service distribué (DDoS) volumétrique jamais enregistrée, atteignant un pic de 11,5 térabits par seconde (Tbps). Ces attaques visent à submerger les cibles avec un volume massif de données, saturant la bande passante et rendant les services inaccessibles aux utilisateurs légitimes.

**Points Clés :**

*   Cloudflare a bloqué plusieurs attaques DDoS "hyper-volumétriques", dont la plus importante a atteint 11,5 Tbps et 5,1 milliards de paquets par seconde (Bpps).
*   L'attaque la plus significative, d'une durée d'environ 35 secondes, était une inondation UDP provenant principalement de Google Cloud.
*   Cette performance dépasse les records précédents de 7,3 Tbps en juin et 3,8 Tbps en octobre 2024, tous deux bloqués par Cloudflare.
*   Microsoft a également fait face à une attaque de 3,47 Tbps en janvier 2022 et à une perturbation mondiale de ses services en juillet 2024.
*   Cloudflare a signalé une augmentation significative du nombre d'attaques DDoS en 2024, avec une hausse de 198% d'un trimestre à l'autre et de 358% d'une année à l'autre. L'entreprise a neutralisé 21,3 millions d'attaques ciblant ses clients et 6,6 millions d'attaques contre sa propre infrastructure au cours d'une campagne de 18 jours.

**Vulnérabilités :**

L'article ne mentionne pas de CVE spécifiques pour cette attaque particulière. Cependant, le type d'attaque décrit est une **inondation UDP (UDP flood)**, qui exploite le protocole UDP pour saturer la bande passante de la cible.

**Recommandations :**

Bien que l'article se concentre sur la défense de Cloudflare, il souligne implicitement l'importance des mesures de sécurité robustes pour contrer les attaques DDoS volumétriques. Pour les organisations, cela inclut :

*   La mise en place de solutions de protection DDoS avancées capables de détecter et de dévier le trafic malveillant.
*   L'optimisation de la capacité réseau pour absorber les pics de trafic.
*   La surveillance continue du trafic réseau pour identifier les anomalies.
*   La diversification des fournisseurs d'infrastructure pour réduire les points de défaillance uniques.

---
[Source](https://www.bleepingcomputer.com/news/security/cloudflare-blocks-record-breaking-115-tbps-ddos-attack/){:target="_blank"}
