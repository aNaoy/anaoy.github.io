---
title: 'RCS and DNS: The NAPTR Record, (Mon, Jul 6th)'
date: 2026-07-06
permalink: /posts/2026/07/06/rcs-and-dns-the-naptr-record-mon-jul-6th/
tags:
- veille-cyber
- sans-isc
---
### Analyse du rôle des enregistrements DNS NAPTR dans le protocole RCS

Le protocole **RCS (Rich Communication Services)**, conçu pour remplacer le SMS, repose sur une infrastructure IP moderne utilisant SIP pour l'établissement des connexions. Une observation récente du trafic réseau met en évidence l'utilisation croissante des enregistrements DNS **NAPTR (Naming Authority Pointer)** dans ce cadre.

**Points clés :**
*   **Fonctionnement :** Contrairement aux enregistrements A ou SRV classiques, le champ NAPTR (RFC 2915) permet une résolution complexe via des expressions régulières pour transformer des chaînes de caractères en noms de domaine.
*   **Usage dans RCS :** Dans les implémentations actuelles, les requêtes NAPTR servent à localiser des services SIP sécurisés (SIPS+D2T). Le processus DNS enchaîne une requête NAPTR pour identifier le protocole de transport, suivie d'une requête SRV pour localiser le serveur cible, et enfin d'une résolution A/AAAA standard.
*   **Flexibilité :** L'usage actuel de NAPTR pour RCS utilise souvent des expressions régulières vides pour simplifier le routage vers des enregistrements SRV, mais le potentiel technique du protocole est beaucoup plus vaste.

**Vulnérabilités :**
*   Aucune vulnérabilité spécifique n'est listée avec un identifiant CVE dans cet article.
*   **Risque potentiel :** L'utilisation d'expressions régulières dans le DNS pour réécrire des enregistrements constitue une surface d'attaque théorique intéressante pour les chercheurs en sécurité, en raison de la complexité intrinsèque de ces traitements côté client.

**Recommandations :**
*   **Surveillance réseau :** Il est conseillé aux administrateurs de surveiller le trafic DNS pour détecter des anomalies dans les requêtes NAPTR, un type d'enregistrement peu courant mais désormais essentiel pour les communications mobiles modernes.
*   **Analyse de sécurité :** Les auditeurs et pentesters devraient porter une attention particulière à la manière dont les clients traitent les réponses NAPTR, notamment si des expressions régulières complexes étaient utilisées à l'avenir, afin d'éviter des risques d'injection ou de détournement de redirection.

---
[Source](https://isc.sans.edu/diary/rss/33124){:target="_blank"}
