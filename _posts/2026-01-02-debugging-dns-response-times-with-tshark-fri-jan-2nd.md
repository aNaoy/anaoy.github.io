---
title: 'Debugging DNS response times with tshark, (Fri, Jan 2nd)'
date: 2026-01-02
permalink: /posts/2026/01/02/debugging-dns-response-times-with-tshark-fri-jan-2nd/
tags:
- veille-cyber
- sans-isc
---
**Analyse des ralentissements de chargement de sites web via DNS**

Des lenteurs inhabituelles lors du chargement de sites web ont été observées, notamment lors de la première connexion de la journée. Après avoir exclu les filtres publicitaires et autres outils de sécurité, la suspicion s'est portée sur le système DNS.

L'utilisation de l'outil `tshark` a permis d'analyser le trafic DNS. Un premier bilan a montré un équilibre entre requêtes et réponses, indiquant qu'aucun problème majeur ne semblait affecter le fonctionnement global du DNS. L'analyse des types de requêtes a révélé une forte présence de requêtes PTR, identifiées comme provenant d'un serveur NTP configuré pour effectuer des recherches inversées sur toutes les connexions. Cette configuration, potentiellement par défaut, a été désactivée, améliorant la distribution des requêtes. Les requêtes SOA, IXFR, AXFR, ainsi que les requêtes DNSSEC (DS, DNSKEY, NSEC/NSEC3) sont liées à des zones internes mises à jour dynamiquement et à la validation DNSSEC activée sur le résolveur récursif.

L'examen des temps de réponse DNS a mis en évidence un temps de réponse maximal de près de 8 secondes, tandis que la moyenne était de 33 ms. Une investigation plus poussée avec la commande `tshark -nr dns.pcap -Y 'dns.flags.response==1' -T fields -e dns.time -e dns.qry.name -e ip.src | sort -n` a permis d'identifier les requêtes les plus lentes. Les requêtes concernant "firmware.zwave-js.io" et "ywab.reader.qq.com" sont apparues comme responsables des plus longs délais.

La comparaison des performances de différents serveurs DNS forwards (1.1.1.1, 8.8.8.8, 9.9.9.9 et le serveur ISP 75.75.75.75) a montré des résultats moyens, médians et des variances très similaires, suggérant une infrastructure sous-jacente comparable pour ces services.

La principale cause identifiée des lenteurs est la surcharge générée par les requêtes PTR non nécessaires du serveur NTP, qui se traduisent souvent par des délais d'attente.

**Points Clés :**
* Des lenteurs de chargement de sites web initialement inexpliquées.
* L'outil `tshark` est efficace pour l'analyse du trafic DNS.
* L'excès de requêtes PTR d'un serveur NTP configuré pour des recherches inversées est identifié comme une cause potentielle de ralentissement.
* Les serveurs DNS forwards couramment utilisés présentent des performances similaires.

**Vulnérabilités :**
* Aucune vulnérabilité spécifique avec un identifiant CVE n'est mentionnée dans cet article. Le problème identifié concerne une mauvaise configuration plutôt qu'une faille de sécurité exploitable.

**Recommandations :**
* Examiner et désactiver les recherches inversées inutiles sur les serveurs NTP.
* Utiliser `tshark` pour analyser le trafic DNS et identifier les problèmes de performance liés aux temps de réponse.
* Vérifier la configuration des serveurs DNS internes et externes pour optimiser les performances.

---
[Source](https://isc.sans.edu/diary/rss/32592){:target="_blank"}
