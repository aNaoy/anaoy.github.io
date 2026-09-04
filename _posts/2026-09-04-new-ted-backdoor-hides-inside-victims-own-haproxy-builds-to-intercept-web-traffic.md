---
title: 'New Ted Backdoor Hides Inside Victims Own HAProxy Builds to Intercept Web Traffic'
date: 2026-09-04
permalink: /posts/2026/09/04/new-ted-backdoor-hides-inside-victims-own-haproxy-builds-to-intercept-web-traffic/
tags:
- veille-cyber
- hackernews
---
### Le backdoor « ted » : une menace furtive au sein de HAProxy

Des acteurs étatiques nord-coréens ciblent des organisations sud-coréennes en déployant un backdoor nommé **ted**, intégré directement dans des versions trojanisées du logiciel de répartition de charge **HAProxy**. Ce mécanisme permet d'intercepter le trafic web, d'exécuter des commandes à distance et de modifier les réponses HTTP sans laisser de traces dans les journaux serveurs.

**Points clés :**
*   **Furtivité absolue :** Le malware manipule les compteurs de connexion de HAProxy pour masquer les requêtes de commande et de contrôle (C2), les rendant invisibles aux outils de monitoring standards.
*   **Mode opératoire :** Le backdoor s'active via des requêtes spécifiques (User-Agent, URL, referer) ou une clé secrète dans l'en-tête `Accept-Language`.
*   **Persistance :** Le kit comprend également des versions modifiées de binaires système (sshd, agetty, atd, polkitd) et un RAT nommé « curlRAT » pour le maintien de l'accès.
*   **Attribution :** Bien que non définitive, l'activité est liée avec une confiance moyenne à des groupes APT nord-coréens (potentiellement APT37, Lazarus ou Kimsuky).

**Vulnérabilités :**
*   Il ne s'agit pas d'une vulnérabilité logicielle (CVE) dans HAProxy, mais d'une **compromission d'intégrité binaire**. Les attaquants exploitent des accès initiaux (potentiellement via des portails Groupware vulnérables) pour remplacer le binaire légitime HAProxy par une version malveillante sur des systèmes non mis à jour (ex: version 2.8.12).

**Recommandations :**
*   **Intégrité des fichiers :** Mettre en place des mécanismes de contrôle de l'intégrité des binaires critiques via des sommes de contrôle robustes et une surveillance des modifications non autorisées dans `/usr/bin/` et `/usr/sbin/`.
*   **Analyse comportementale :** Privilégier l'analyse comportementale de la mémoire plutôt que la simple vérification des versions de logiciels, car un binaire trojanisé peut conserver la même chaîne de version qu'un build sain.
*   **Corrélation réseau :** Effectuer une corrélation indépendante du trafic réseau pour identifier les anomalies entre les logs applicatifs (souvent manipulés par le malware) et le trafic réel observé sur le segment réseau.
*   **Mise à jour :** Maintenir HAProxy à jour vers les dernières versions stables pour corriger les vulnérabilités connues, bien que la mise à jour seule ne suffise pas à supprimer le backdoor si le système est déjà compromis.

---
[Source](https://thehackernews.com/2026/09/new-ted-backdoor-hides-inside-victims.html){:target="_blank"}
