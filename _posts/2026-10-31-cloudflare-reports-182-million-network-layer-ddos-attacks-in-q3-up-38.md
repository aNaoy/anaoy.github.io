---
title: 'Cloudflare Reports 18.2 Million Network-Layer DDoS Attacks in Q3, Up 38%'
date: 2026-10-31
permalink: /posts/2026/10/31/cloudflare-reports-182-million-network-layer-ddos-attacks-in-q3-up-38/
tags:
- veille-cyber
- hackernews
---
### Recrudescence des attaques DDoS au troisième trimestre 2026

Le rapport trimestriel de Cloudflare révèle une augmentation massive des attaques par déni de service distribué (DDoS). Au troisième trimestre 2026, l'entreprise a neutralisé 18,2 millions d'attaques au niveau réseau (couche 3) et 14,4 billions de requêtes HTTP, soit une attaque toutes les 0,44 seconde.

**Points clés :**
* **Hausse globale :** Le nombre d'attaques réseau a progressé de 38 % par rapport au trimestre précédent.
* **Nouvelles tactiques :** Les attaques de courte durée (moins de 10 minutes) et à faible débit (moins de 1 Gbps) ont bondi de 208 %.
* **Mutation des vecteurs :** Si les attaques hyper-volumétriques (> 1 Tbps) diminuent grâce au démantèlement de réseaux de botnets par les autorités, les attaques par amplification DNS ont progressé de 215 %.
* **Menaces émergentes :** Apparition de nouveaux botnets basés sur l'IoT, tels que *Dysphoria* et *Evooo1Bot*.
* **Cibles privilégiées :** Les secteurs des médias, de l'informatique, des télécommunications et des jeux d'argent sont les plus touchés. Les États-Unis, la Chine et l'Indonésie restent les pays les plus visés.

**Vulnérabilités et vecteurs identifiés :**
* **Exploitation de services :** Utilisation intensive de services "DDoS-for-hire" (stresser/booter).
* **Amplification DNS :** Vecteur en forte croissance utilisant des serveurs mal configurés pour multiplier le trafic vers la cible.
* **Botnets IoT :** Utilisation de dispositifs connectés vulnérables (souvent via l'exploitation de failles connues non corrigées sur des systèmes Linux).

**Recommandations :**
* **Surveillance proactive :** Mettre en œuvre des solutions de protection DDoS capables de détecter les attaques de type "flash" (très courtes durées).
* **Sécurisation des actifs :** Patching rigoureux des dispositifs IoT et des serveurs Linux pour prévenir l'enrôlement dans des botnets.
* **Filtrage réseau :** Configurer les serveurs DNS pour limiter les risques d'amplification (désactivation des résolveurs ouverts).
* **Protection adaptative :** S'appuyer sur des services de nettoyage (scrubbing) cloud capables de bloquer les attaques volumétriques et protocolaires en temps réel avant qu'elles n'atteignent l'infrastructure.

---
[Source](https://thehackernews.com/2026/10/cloudflare-reports-182-million-network.html){:target="_blank"}
