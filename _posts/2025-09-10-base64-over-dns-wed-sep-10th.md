---
title: 'BASE64 Over DNS, (Wed, Sep 10th)'
date: 2025-09-10
permalink: /posts/2025/09/10/base64-over-dns-wed-sep-10th/
tags:
- veille-cyber
- sans-isc
---
## Utilisation du BASE64 dans les étiquettes DNS pour la communication furtive

Un agent malveillant peut exploiter le protocole DNS pour établir un canal de commande et de contrôle (C2) en utilisant le codage BASE64 dans les étiquettes de noms de domaine. Bien que les standards DNS (RFC 1035) limitent les caractères autorisés dans les étiquettes (alphanumériques et le trait d'union), certains outils d'interrogation DNS, comme `nslookup`, ne valident pas strictement ces formats lors de la transmission des requêtes. Cela permet d'inclure des caractères spéciaux comme '+', '/' et '=' qui font partie de l'alphabet BASE64.

Cependant, cette méthode n'est pas universellement compatible. Les API Windows standard pour la résolution de noms, utilisées par des utilitaires comme `ping` ou directement par la `DnsApi`, refusent les requêtes contenant ces caractères spéciaux, générant des erreurs spécifiques (comme l'erreur 9560 pour les caractères '+', '/' et '='). Par conséquent, un agent malveillant utilisant cette technique de communication via DNS devrait interagir directement avec le serveur DNS, sans passer par les interfaces de résolution de noms classiques du système d'exploitation.

Il est conseillé de surveiller les journaux DNS à la recherche d'étiquettes de noms de domaine contenant des caractères inhabituels ou spéciaux, car cela pourrait indiquer une tentative de communication C2 dissimulée.

**Points clés :**

*   Les agents malveillants peuvent utiliser le codage BASE64 dans les étiquettes DNS pour la communication C2.
*   Certains outils DNS (ex: `nslookup`) permettent l'utilisation de caractères spéciaux non conformes aux standards RFC.
*   Les API Windows standard de résolution DNS bloquent ces caractères spéciaux.

**Vulnérabilités :**

*   Les implémentations du protocole DNS qui ne valident pas strictement le format des étiquettes peuvent être exploitées.
*   Le manque de détection des caractères non standard dans les requêtes DNS par certains systèmes.

**Recommandations :**

*   Analyser les journaux DNS pour identifier les requêtes contenant des caractères spéciaux dans les étiquettes de noms de domaine.
*   S'assurer que les infrastructures DNS et les outils de résolution de noms appliquent une validation stricte des étiquettes conformes aux standards RFC.

---
[Source](https://isc.sans.edu/diary/rss/32274){:target="_blank"}
